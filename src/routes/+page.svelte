<script lang="ts">
	import { onMount } from 'svelte';

    // Trusted by security organizations
    const partners = [
        { name: 'International NGO', src: '' },
        { name: 'Global Security Firm', src: '' },
        { name: 'Risk Management', src: '' },
        { name: 'Physical Security Co.', src: '' },
        { name: 'Intelligence Agency', src: '' },
        { name: 'Security Operations', src: '' },
    ];

    const insights = [
        {
            tag: 'Case Study',
            title: 'NGO Operations in High-Risk Regions',
            desc: 'How autonomous intelligence monitoring reduced analyst workload by 80% while improving threat detection.',
            bg: 'bg-gray-50'
        },
        {
            tag: 'Intelligence Brief',
            title: 'Real-Time Threat Detection',
            desc: 'Monitoring thousands of sources continuously to identify emerging risks before they escalate.',
            bg: 'bg-gray-100'
        },
        {
            tag: 'Use Case',
            title: 'Security Firms in Emerging Markets',
            desc: 'Transforming scattered signals into actionable intelligence for physical security operations.',
            bg: 'bg-gray-50'
        },
        {
            tag: 'Platform',
            title: 'Autonomous Intel Agents',
            desc: 'AI agents that understand operational workflows and deliver mission-ready intelligence.',
            bg: 'bg-gray-100'
        }
    ];

    const testimonials = [
        {
            quote: "SentryCode gives us the intelligence capacity we need without the analyst headcount. It's transformed how we operate in high-risk environments.",
            author: "Security Operations Director",
            role: "Head of Intelligence",
            company: "International NGO",
            img: "/generated/image-confident-security-director-in-tactical--1765522994337-1.webp"
        }
    ];

    const features = [
        {
            title: "Autonomous Monitoring",
            description: "AI agents monitor thousands of global sources continuously, 24/7, without human intervention.",
            icon: "monitor"
        },
        {
            title: "Mission-Ready Intelligence",
            description: "Transform scattered signals into actionable intelligence that fits your operational workflows.",
            icon: "target"
        },
        {
            title: "Real-Time Alerts",
            description: "Get notified of emerging threats and critical events as they happen, not hours later.",
            icon: "alert"
        },
        {
            title: "Analyst Augmentation",
            description: "Overcome analyst capacity constraints with AI that understands security operations.",
            icon: "team"
        }
    ];
</script>

<div class="min-h-screen bg-white text-gray-900 font-sans selection:bg-gray-200">
    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-sm border-b border-gray-100">
        <div class="max-w-[1600px] mx-auto px-6 py-6 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <svg class="w-8 h-8 text-gray-900" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                        fill="currentColor"
                    />
                </svg>
                <a href="/" class="text-lg font-semibold tracking-tight text-gray-900">
                    SentryCode
                </a>
            </div>
            <div>
                <a href="#contact" class="bg-gray-900 text-white px-5 py-2.5 text-xs font-medium rounded-sm hover:bg-gray-800 transition-colors">
                    Request Demo
                </a>
            </div>
        </div>
    </header>

    <main class="pt-32 pb-20">
        <div class="max-w-[1600px] mx-auto px-6 grid grid-cols-12 gap-8">
            <!-- Sidebar Navigation -->
            <div class="col-span-2 hidden lg:block sticky top-32 h-fit">
                <nav class="flex flex-col space-y-3 text-xs text-gray-500 font-medium">
                    <a href="#" class="text-gray-900">Home</a>
                    <a href="#platform" class="hover:text-gray-900 transition-colors">Platform</a>
                    <a href="#intelligence" class="hover:text-gray-900 transition-colors">Intelligence</a>
                    <a href="#insights" class="hover:text-gray-900 transition-colors">Insights</a>
                    <a href="#contact" class="hover:text-gray-900 transition-colors">Contact</a>
                </nav>
            </div>

            <!-- Main Content Area -->
            <div class="col-span-12 lg:col-span-10 space-y-32">
                
                <!-- Hero Section -->
                <section class="relative">
                    <div class="relative w-full h-[600px] overflow-hidden rounded-sm bg-gray-950">
                        <!-- Operations Center Background -->
                        <img src="/generated/image-professional-security-operations-center--1765522990608-0.webp" alt="Security Operations Center" class="absolute inset-0 w-full h-full object-cover opacity-60" />
                        
                        <div class="absolute inset-0 bg-gradient-to-t from-gray-950 via-gray-950/50 to-transparent"></div>
                        
                        <div class="absolute inset-0 flex flex-col items-center justify-center p-12 text-center">
                            <h1 class="text-4xl md:text-5xl font-normal text-white mb-6 max-w-3xl leading-tight">
                                Transform scattered signals into<br>mission-ready intelligence
                            </h1>
                            <p class="text-lg text-gray-300 mb-12 max-w-2xl">
                                Autonomous agents monitoring thousands of sources continuously for security operations in high-risk regions
                            </p>

                            <!-- Trust Badge -->
                            <div class="bg-white/95 backdrop-blur-sm p-8 rounded-sm shadow-sm max-w-4xl w-full">
                                <p class="text-[10px] text-gray-500 mb-6 uppercase tracking-wide">
                                    Trusted by security operations teams and NGOs operating in high-risk environments
                                </p>
                                <div class="grid grid-cols-2 md:grid-cols-3 gap-8 items-center justify-items-center opacity-60">
                                    {#each partners as partner}
                                        <div class="h-6 flex items-center justify-center">
                                            <span class="text-[10px] font-semibold text-gray-700">{partner.name}</span>
                                        </div>
                                    {/each}
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- How SentryCode Works Section -->
                <section id="platform">
                    <div class="flex justify-between items-baseline mb-24 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900 max-w-xl leading-tight">
                            Autonomous intelligence for security operations
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Platform</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-16 mb-24">
                        {#each features as feature}
                            <div class="space-y-4">
                                <div class="w-12 h-12 bg-gray-900 rounded-sm flex items-center justify-center">
                                    {#if feature.icon === 'monitor'}
                                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                                        </svg>
                                    {:else if feature.icon === 'target'}
                                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                                        </svg>
                                    {:else if feature.icon === 'alert'}
                                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" />
                                        </svg>
                                    {:else}
                                        <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                                        </svg>
                                    {/if}
                                </div>
                                <h3 class="text-xl font-medium text-gray-900">{feature.title}</h3>
                                <p class="text-sm text-gray-600 leading-relaxed">{feature.description}</p>
                            </div>
                        {/each}
                    </div>

                    <!-- Platform Image -->
                    <div class="relative w-full h-[400px] rounded-sm overflow-hidden bg-gray-950">
                        <img src="/generated/image-global-satellite-view-of-earth-at-night--1765522997261-3.webp" alt="Global Intelligence Network" class="absolute inset-0 w-full h-full object-cover opacity-70" />
                        <div class="absolute inset-0 bg-gradient-to-t from-gray-950 via-transparent to-transparent"></div>
                        <div class="absolute bottom-0 left-0 right-0 p-12">
                            <p class="text-white text-lg font-light max-w-2xl">
                                Monitoring thousands of global sources continuously to identify threats and opportunities before they escalate
                            </p>
                        </div>
                    </div>
                </section>

                <!-- Intelligence Market Section -->
                <section id="intelligence">
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Capturing the $8B intelligence market
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Market Opportunity</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-12 text-sm leading-relaxed text-gray-600 mb-24">
                        <div class="space-y-6">
                            <p class="font-medium text-gray-900">
                                Security operations teams in high-risk regions face an impossible challenge.
                            </p>
                            <p>
                                They need real-time intelligence to protect their people and operations, but lack the analyst capacity to monitor thousands of sources continuously. Traditional intelligence services are too expensive and too slow.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                SentryCode transforms scattered global signals into mission-ready intelligence via autonomous agents. Our AI understands operational workflows and delivers actionable insights that security teams can act on immediately.
                            </p>
                            <p>
                                Starting with security firms and NGOs in high-risk regions, we're capturing the $8B intelligence market by automating what previously required teams of analysts.
                            </p>
                        </div>
                        <div class="space-y-6">
                            <p>
                                Our go-to-market strategy targets security directors at NGOs and physical security companies through risk management forums, overcoming analyst cost concerns with automated intelligence workflows.
                            </p>
                            <p class="font-medium text-gray-900">
                                The result: Intelligence capacity without the headcount.
                            </p>
                        </div>
                    </div>

                    <!-- Analyst Image -->
                    <div class="relative w-full h-[400px] rounded-sm overflow-hidden">
                        <img src="/generated/image-professional-analyst-reviewing-intellige-1765523075635-0.webp" alt="Intelligence Analysis" class="absolute inset-0 w-full h-full object-cover" />
                        <div class="absolute inset-0 bg-gradient-to-r from-gray-900/80 to-transparent"></div>
                        <div class="absolute inset-0 flex items-center p-12">
                            <div class="max-w-xl">
                                <p class="text-white text-2xl font-light mb-4">
                                    "Intelligence that understands operational workflows"
                                </p>
                                <p class="text-gray-300 text-sm">
                                    Autonomous agents that monitor, analyze, and deliver mission-ready intelligence 24/7
                                </p>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Founders Section -->
                <section class="bg-gray-950 text-white rounded-sm overflow-hidden relative min-h-[400px] flex items-center">
                    <!-- Background Pattern -->
                    <div class="absolute inset-0 opacity-10">
                        <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="none">
                            <defs>
                                <pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse">
                                    <path d="M 10 0 L 0 0 0 10" fill="none" stroke="currentColor" stroke-width="0.5"/>
                                </pattern>
                            </defs>
                            <rect width="100" height="100" fill="url(#grid)" />
                        </svg>
                    </div>

                    <div class="relative z-10 p-16 w-full">
                        <div class="mb-12">
                            <h2 class="text-3xl font-light mb-6">
                                Built by security and intelligence experts
                            </h2>
                            <p class="text-sm text-gray-400 max-w-2xl">
                                Our founding team combines deep expertise in security operations, intelligence analysis, and AI systems.
                            </p>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                            <div class="space-y-2">
                                <div class="font-medium text-lg">Richard Wilson</div>
                                <div class="text-sm text-gray-400">CEO & Cofounder</div>
                            </div>
                            <div class="space-y-2">
                                <div class="font-medium text-lg">Stefan Raath</div>
                                <div class="text-sm text-gray-400">CTO & Cofounder</div>
                            </div>
                            <div class="space-y-2">
                                <div class="font-medium text-lg">Paul Stukel</div>
                                <div class="text-sm text-gray-400">Strategy & Cofounder</div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Testimonials -->
                <section>
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Trusted by security operations teams
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Testimonials</span>
                    </div>

                    <div class="relative">
                        <div class="flex gap-8 overflow-hidden">
                            <div class="w-full md:w-[800px] shrink-0 bg-gray-50 flex">
                                <div class="w-1/3 shrink-0">
                                    <img src="/generated/image-confident-security-director-in-tactical--1765522994337-1.webp" alt="Security Director" class="w-full h-full object-cover" />
                                </div>
                                <div class="w-2/3 p-12 flex flex-col justify-center">
                                    <blockquote class="text-xl font-light leading-relaxed mb-8">
                                        "SentryCode gives us the intelligence capacity we need without the analyst headcount. It's transformed how we operate in high-risk environments."
                                    </blockquote>
                                    <div class="mt-2">
                                        <div class="font-medium">Security Operations Director</div>
                                        <div class="text-xs text-gray-500">Head of Intelligence, International NGO</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Intelligence Insights -->
                <section id="insights">
                    <div class="flex justify-between items-baseline mb-16 border-b border-gray-100 pb-4">
                        <h2 class="text-3xl font-light text-gray-900">
                            Intelligence insights
                        </h2>
                        <span class="text-[10px] text-gray-400 uppercase tracking-wider">Resources</span>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                        {#each insights as insight}
                            <div class="group cursor-pointer">
                                <div class="relative aspect-square mb-6 overflow-hidden {insight.bg} flex items-center justify-center rounded-sm">
                                    <span class="absolute top-4 left-4 text-[10px] uppercase tracking-wider bg-white/90 px-2 py-1 backdrop-blur-sm font-medium">{insight.tag}</span>
                                    <div class="text-center p-8">
                                        <svg class="w-16 h-16 mx-auto text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                                        </svg>
                                    </div>
                                </div>
                                <h3 class="text-lg font-normal mb-3 leading-tight group-hover:underline decoration-1 underline-offset-4">
                                    {insight.title}
                                </h3>
                                <p class="text-xs text-gray-500 mb-4 leading-relaxed">
                                    {insight.desc}
                                </p>
                                <a href="#" class="text-xs font-medium underline decoration-1 underline-offset-4">Learn more</a>
                            </div>
                        {/each}
                    </div>
                </section>

            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-white pt-32 pb-12 border-t border-gray-100 relative overflow-hidden">
        <!-- Large Background Watermark -->
        <div class="absolute left-0 bottom-0 text-[20vw] font-bold text-gray-50 leading-none select-none pointer-events-none -mb-12 -ml-12">
            SC
        </div>

        <div class="max-w-[1600px] mx-auto px-6 relative z-10">
            <div class="flex flex-col md:flex-row justify-between items-end md:items-center mb-24" id="contact">
                <div class="text-lg font-light">Mission-ready intelligence</div>
                <div class="text-lg font-light underline decoration-1 underline-offset-4">SENTRYCODE.COM</div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-end">
                <div class="md:col-span-6">
                    <!-- Logo -->
                    <div class="flex items-center gap-4 mb-4">
                        <svg class="w-8 h-8 text-gray-900" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                fill-rule="evenodd"
                                clip-rule="evenodd"
                                d="M6.99251 12.196C6.85314 12.5757 6.62925 12.9208 6.33682 13.2067H6.33835C6.00191 13.5351 5.58566 13.7756 5.12816 13.9059C4.67065 14.0362 4.18671 14.0522 3.72118 13.9523C3.25564 13.8524 2.82357 13.64 2.46501 13.3345C2.10645 13.0291 1.83299 12.6406 1.66998 12.2051C1.50697 11.7696 1.45969 11.3012 1.5325 10.8432C1.60532 10.3852 1.79587 9.95244 2.08653 9.58516C2.37718 9.21781 2.75852 8.9277 3.1952 8.74177C3.63188 8.55585 4.10979 8.48002 4.58462 8.52142L4.57074 8.50792C5.0567 8.54782 5.54575 8.48407 6.00378 8.32124C6.4618 8.15846 6.87776 7.90043 7.2226 7.56521C7.56746 7.22998 7.83285 6.82564 8.00036 6.38041C8.16786 5.93517 8.23344 5.45976 8.1924 4.98737L8.20628 5.00087C8.15181 4.43594 8.27796 3.86844 8.56753 3.37575C8.85701 2.88307 9.29579 2.48919 9.82407 2.24782C10.3523 2.00645 10.9443 1.92933 11.5192 2.02701C12.0942 2.12467 12.6243 2.39237 13.037 2.79358C13.4497 3.19479 13.7251 3.70999 13.8256 4.26892C13.926 4.82785 13.8467 5.4033 13.5984 5.9168C13.3501 6.4303 12.9449 6.85685 12.4381 7.13828C11.9313 7.41971 11.3474 7.54233 10.7663 7.4894L10.781 7.5029C10.2949 7.46279 9.80563 7.52632 9.34741 7.68904C8.88919 7.85176 8.47309 8.10975 8.12805 8.44499C7.78301 8.78025 7.51742 9.18466 7.34983 9.63001C7.18224 10.0754 7.11669 10.551 7.15774 11.0235L7.14309 11.01C7.1833 11.4112 7.13189 11.8162 6.99251 12.196ZM11.5077 14.7121L11.493 14.6986C11.9061 14.739 12.3232 14.6897 12.7143 14.5543C13.1053 14.4188 13.4605 14.2007 13.7542 13.9154C14.0477 13.6302 14.2726 13.285 14.4121 12.905C14.5518 12.525 14.6028 12.1196 14.5615 11.718L14.5762 11.7315C14.5351 11.2591 14.6007 10.7838 14.7681 10.3385C14.9356 9.89327 15.2011 9.48893 15.5459 9.15368C15.8908 8.8185 16.3068 8.56042 16.7648 8.39767C17.2228 8.23481 17.7118 8.17111 18.1978 8.21099L18.1832 8.19749C18.7645 8.25059 19.3485 8.12801 19.8556 7.84656C20.3627 7.56511 20.7681 7.13845 21.0165 6.62479C21.265 6.11114 21.3444 5.53548 21.2439 4.97634C21.1435 4.4172 20.868 3.9018 20.4551 3.50044C20.0422 3.09909 19.512 2.8313 18.9368 2.73364C18.3616 2.63596 17.7695 2.71315 17.241 2.95467C16.7126 3.19618 16.2737 3.59027 15.9842 4.08319C15.6946 4.57609 15.5685 5.14383 15.6232 5.70895L15.6093 5.6947C15.6504 6.16712 15.585 6.64259 15.4175 7.08788C15.2501 7.53318 14.9846 7.93758 14.6398 8.27287C14.2949 8.60805 13.8789 8.86612 13.4208 9.02888C12.9627 9.19163 12.4736 9.25523 11.9876 9.21526L12.0015 9.22951C11.5885 9.18908 11.1713 9.23836 10.7803 9.37381C10.3893 9.50919 10.034 9.72744 9.74039 10.0127C9.44674 10.2979 9.22199 10.6431 9.08234 11.0231C8.94276 11.4031 8.89176 11.8085 8.93304 12.2101L8.91915 12.1966C8.96005 12.6689 8.89439 13.1443 8.72688 13.5895C8.5593 14.0346 8.29389 14.4389 7.94908 14.7741C7.60425 15.1093 7.18835 15.3673 6.73039 15.5302C6.27242 15.693 5.78342 15.7569 5.29749 15.7171L5.31138 15.7306C4.73003 15.6775 4.14599 15.8001 3.63892 16.0815C3.13186 16.363 2.72644 16.7896 2.478 17.3033C2.22954 17.817 2.15013 18.3926 2.25061 18.9518C2.35109 19.5109 2.62657 20.0263 3.03945 20.4276C3.45234 20.829 3.98253 21.0968 4.55773 21.1944C5.13293 21.2921 5.72512 21.2149 6.25353 20.9734C6.78193 20.7319 7.22085 20.3379 7.51038 19.8449C7.79994 19.352 7.92601 18.7843 7.87139 18.2191L7.88605 18.2326C7.845 17.7602 7.91058 17.2849 8.07809 16.8396C8.24551 16.3944 8.511 15.99 8.85581 15.6548C9.20069 15.3196 9.61664 15.0615 10.0746 14.8988C10.5327 14.7359 11.0217 14.6722 11.5077 14.7121ZM17.1996 10.7633C16.9071 11.0493 16.6832 11.3944 16.5437 11.7741C16.4042 12.1538 16.3526 12.5587 16.3925 12.9601L16.3786 12.9466C16.4197 13.419 16.3541 13.8944 16.1866 14.3396C16.0191 14.7849 15.7537 15.1892 15.4089 15.5244C15.064 15.8596 14.648 16.1177 14.19 16.2804C13.732 16.4433 13.2429 16.507 12.757 16.4671L12.7708 16.4806C12.1896 16.4281 11.6057 16.551 11.0989 16.8328C10.5921 17.1145 10.1871 17.5414 9.93902 18.0551C9.69097 18.5689 9.61188 19.1444 9.71265 19.7035C9.81349 20.2625 10.0892 20.7777 10.5022 21.1788C10.9152 21.5799 11.4454 21.8474 12.0205 21.9448C12.5957 22.0423 13.1877 21.9649 13.716 21.7234C14.2443 21.4817 14.683 21.0877 14.9724 20.5947C15.2618 20.1018 15.3878 19.5342 15.3332 18.9692L15.3478 18.9827C15.3068 18.5103 15.3723 18.0349 15.5398 17.5896C15.7073 17.1444 15.9728 16.7401 16.3176 16.4048C16.6625 16.0696 17.0784 15.8115 17.5364 15.6488C17.9945 15.486 18.4835 15.4222 18.9695 15.4621L18.9548 15.4486C19.4296 15.4901 19.9076 15.4144 20.3444 15.2286C20.7811 15.0427 21.1625 14.7527 21.4533 14.3854C21.744 14.0181 21.9347 13.5854 22.0075 13.1274C22.0805 12.6694 22.0332 12.2009 21.8703 11.7653C21.7073 11.3298 21.4339 10.9413 21.0754 10.6358C20.7168 10.3303 20.2848 10.1178 19.8192 10.0179C19.3536 9.91795 18.8697 9.93385 18.4121 10.0641C17.9546 10.1945 17.5383 10.4349 17.2019 10.7633H17.1996Z"
                                fill="currentColor"
                            />
                        </svg>
                        <div class="text-sm font-semibold">
                            SentryCode
                        </div>
                    </div>
                </div>
                
                <div class="md:col-span-6 flex flex-col md:flex-row justify-between items-end md:items-end gap-8">
                    <div class="text-[10px] text-gray-400">
                        © 2025 SentryCode
                    </div>
                    
                    <div class="flex gap-8 text-[10px] font-medium uppercase tracking-wide">
                        <div class="flex flex-col gap-2">
                            <a href="#platform">Platform</a>
                            <a href="#intelligence">Intelligence</a>
                            <a href="#contact">Contact</a>
                        </div>
                        <div class="flex flex-col gap-2">
                            <a href="#">Terms</a>
                            <a href="#">Privacy</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom scrollbar hide for clean look */
    ::-webkit-scrollbar {
        width: 0px;
        background: transparent;
    }
</style>

