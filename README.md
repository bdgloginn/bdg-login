# bdg-login
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BDG Game - Official Registration & Welcome Bonus</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Outfit:wght@600;700;800&display=swap" rel="stylesheet">
  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>
  
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            display: ['Outfit', 'sans-serif'],
          },
          colors: {
            gold: {
              300: '#FDE047',
              400: '#FACC15',
              500: '#EAB308',
              600: '#CA8A04',
            },
            brandDark: {
              900: '#0B0F19',
              850: '#111827',
              800: '#1A2234',
              700: '#243048',
            }
          },
          boxShadow: {
            'glow-gold': '0 0 25px -3px rgba(234, 179, 8, 0.45)',
            'glow-accent': '0 0 20px -2px rgba(245, 158, 11, 0.3)',
          }
        }
      }
    }
  </script>
  <style>
    /* Smooth gradient shimmering effects */
    .gold-gradient {
      background: linear-gradient(135deg, #FFE259 0%, #FFA751 100%);
    }
    .gold-text-gradient {
      background: linear-gradient(135deg, #FFF099 0%, #F59E0B 50%, #D97706 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .card-glass {
      background: rgba(26, 34, 52, 0.75);
      backdrop-filter: blur(12px);
      border: 1px solid rgba(253, 224, 71, 0.15);
    }
    .pulse-glow {
      animation: pulseAnimation 2.2s infinite;
    }
    @keyframes pulseAnimation {
      0% {
        box-shadow: 0 0 0 0 rgba(234, 179, 8, 0.7);
      }
      70% {
        box-shadow: 0 0 0 14px rgba(234, 179, 8, 0);
      }
      100% {
        box-shadow: 0 0 0 0 rgba(234, 179, 8, 0);
      }
    }
  </style>
</head>
<body class="bg-[#080B11] text-gray-100 font-sans min-h-screen antialiased flex flex-col items-center">

  <!-- Floating Toast Notification -->
  <div id="toast" class="fixed top-5 z-50 transition-all duration-300 opacity-0 pointer-events-none transform -translate-y-5 px-5 py-3 rounded-full bg-emerald-500 text-white font-medium flex items-center gap-2 shadow-xl border border-emerald-400/40 text-sm">
    <i data-lucide="check-circle" class="w-4 h-4 text-white"></i>
    <span>Invite Code copied successfully!</span>
  </div>

  <!-- Top Sticky Quick-Launch Notification Bar -->
  <div class="w-full bg-gradient-to-r from-amber-600 via-yellow-500 to-amber-600 text-black py-2 px-3 text-center text-xs font-bold flex items-center justify-center gap-2 shadow-md">
    <span>⚡ Instant Sign-Up Active:</span>
    <button onclick="openTargetUrl()" class="underline font-extrabold hover:text-white transition-colors cursor-pointer flex items-center gap-1">
      Open Official Register Page <i data-lucide="external-link" class="w-3.5 h-3.5"></i>
    </button>
  </div>

  <!-- Main Container constrained for mobile/tablet elegance -->
  <main class="w-full max-w-md sm:max-w-lg px-4 py-6 md:py-10 flex flex-col items-center">

    <!-- Top Badge & Navigation -->
    <header class="w-full flex items-center justify-between pb-6 mb-2 border-b border-gray-800/80">
      <div class="flex items-center gap-2 cursor-pointer" onclick="openTargetUrl()">
        <div class="w-9 h-9 rounded-xl gold-gradient flex items-center justify-center font-black text-black font-display shadow-md">
          B
        </div>
        <span class="font-display font-extrabold text-xl tracking-wide text-white">
          BDG<span class="text-gold-400">CLUB</span>
        </span>
      </div>
      <button onclick="openTargetUrl()" class="flex items-center gap-1.5 px-3.5 py-1.5 rounded-full bg-gold-500/10 border border-gold-500/30 text-gold-300 text-xs font-semibold hover:bg-gold-500/20 active:scale-95 transition-all">
        <span class="w-2 h-2 rounded-full bg-emerald-400 animate-ping"></span>
        <span>Open Link</span>
      </button>
    </header>

    <!-- Quick Direct Launch Card -->
    <section class="w-full mb-5">
      <div class="bg-gradient-to-r from-amber-500/15 via-yellow-500/10 to-amber-500/15 border border-gold-500/30 rounded-2xl p-3.5 flex items-center justify-between shadow-lg">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-xl bg-gold-400/20 text-gold-400 flex items-center justify-center">
            <i data-lucide="zap" class="w-5 h-5"></i>
          </div>
          <div>
            <h4 class="text-xs font-bold text-white uppercase tracking-wider">Fast Direct Open</h4>
            <p class="text-[11px] text-gray-300">Tap to load registration directly</p>
          </div>
        </div>
        <button 
          onclick="openTargetUrl()" 
          class="px-3.5 py-2 rounded-xl gold-gradient text-slate-950 font-bold text-xs flex items-center gap-1 hover:brightness-110 active:scale-95 transition-all shadow"
        >
          <span>Go Now</span>
          <i data-lucide="arrow-right" class="w-3.5 h-3.5"></i>
        </button>
      </div>
    </section>

    <!-- Hero Section -->
    <section class="text-center w-full mt-2">
      <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-brandDark-800 border border-gold-400/20 text-xs text-amber-300 mb-4 shadow-sm">
        <i data-lucide="flame" class="w-4 h-4 text-amber-400 fill-amber-400"></i>
        <span>Exclusive Official Sign-up Offer</span>
      </div>

      <h1 class="font-display text-3xl sm:text-4xl font-extrabold leading-tight text-white mb-3">
        Register & Claim Your <br>
        <span class="gold-text-gradient">Daily Welcome Bonus</span>
      </h1>

      <p class="text-gray-300 text-sm sm:text-base leading-relaxed max-w-sm mx-auto mb-6">
        Sign up in seconds, claim your registration gifts, and get access to daily check-in rewards & instant withdrawals.
      </p>

      <!-- Invitation Code Box -->
      <div class="card-glass rounded-2xl p-4 sm:p-5 shadow-xl mb-6 relative overflow-hidden text-left">
        <div class="absolute -top-12 -right-12 w-28 h-28 bg-gold-500/10 rounded-full blur-xl pointer-events-none"></div>
        
        <div class="flex items-center justify-between mb-2">
          <span class="text-xs font-semibold uppercase tracking-wider text-gray-400 flex items-center gap-1.5">
            <i data-lucide="key" class="w-3.5 h-3.5 text-gold-400"></i> Official Invitation Code
          </span>
          <span class="text-[11px] text-emerald-400 font-medium bg-emerald-950/60 px-2 py-0.5 rounded border border-emerald-800">
            Auto-Applied
          </span>
        </div>

        <div class="flex items-center gap-2 bg-brandDark-900/90 border border-gold-500/30 rounded-xl p-2 sm:p-2.5">
          <input 
            type="text" 
            id="inviteCode" 
            value="1kuV2648127" 
            readonly 
            class="bg-transparent font-mono font-bold text-lg sm:text-xl text-amber-300 w-full tracking-widest pl-2 outline-none select-all cursor-pointer"
            onclick="copyInvitationCode()"
          />
          <button 
            id="copyBtn" 
            type="button"
            onclick="copyInvitationCode()" 
            class="px-4 py-2.5 rounded-lg gold-gradient font-bold text-gray-950 text-xs sm:text-sm flex items-center gap-1.5 hover:opacity-95 active:scale-95 transition-all shadow cursor-pointer whitespace-nowrap"
            aria-label="Copy invitation code"
          >
            <i data-lucide="copy" class="w-4 h-4"></i>
            <span>Copy</span>
          </button>
        </div>
        <p class="text-[11px] text-gray-400 mt-2 text-center">
          Tap <strong class="text-gray-300 font-semibold">Copy</strong> or click below to open the registration page directly with code attached.
        </p>
      </div>

      <!-- Main CTA Button -->
      <a 
        href="https://bdg4.vip//#/register?invitationCode=1kuV2648127" 
        target="_blank" 
        rel="noopener noreferrer"
        onclick="trackAndOpen(event)"
        class="pulse-glow block w-full py-4 px-6 rounded-2xl gold-gradient text-slate-950 font-display font-extrabold text-lg tracking-wide shadow-glow-gold hover:brightness-105 active:scale-[0.98] transition-all flex items-center justify-center gap-2.5 text-center group cursor-pointer"
      >
        <span>Register & Claim Bonus</span>
        <i data-lucide="arrow-right" class="w-5 h-5 transition-transform group-hover:translate-x-1"></i>
      </a>

      <!-- Quick Highlights Ticker -->
      <div class="grid grid-cols-3 gap-2 mt-5 text-center">
        <div class="bg-brandDark-850/70 border border-gray-800 rounded-xl p-2.5">
          <span class="block text-amber-400 font-display font-bold text-base sm:text-lg">Fast</span>
          <span class="text-[11px] text-gray-400">Withdrawals</span>
        </div>
        <div class="bg-brandDark-850/70 border border-gray-800 rounded-xl p-2.5">
          <span class="block text-amber-400 font-display font-bold text-base sm:text-lg">24/7</span>
          <span class="text-[11px] text-gray-400">Live Support</span>
        </div>
        <div class="bg-brandDark-850/70 border border-gray-800 rounded-xl p-2.5">
          <span class="block text-amber-400 font-display font-bold text-base sm:text-lg">Daily</span>
          <span class="text-[11px] text-gray-400">Cash Rewards</span>
        </div>
      </div>
    </section>

    <!-- 3-Step Registration Guide -->
    <section class="w-full mt-10">
      <div class="flex items-center gap-2 mb-4">
        <i data-lucide="user-plus" class="w-5 h-5 text-gold-400"></i>
        <h2 class="font-display font-bold text-lg text-white">How to Register in 3 Steps</h2>
      </div>

      <div class="space-y-3">
        <!-- Step 1 -->
        <div class="card-glass rounded-xl p-3.5 flex items-start gap-3.5 border-l-4 border-l-gold-400 cursor-pointer hover:border-gold-300 transition-all" onclick="openTargetUrl()">
          <div class="w-7 h-7 rounded-full bg-gold-400/20 text-gold-400 font-bold flex items-center justify-center text-xs flex-shrink-0 mt-0.5">
            1
          </div>
          <div>
            <h3 class="font-semibold text-sm text-gray-100 flex items-center gap-1.5">
              <span>Open Link & Enter Phone</span>
              <i data-lucide="external-link" class="w-3.5 h-3.5 text-gold-400"></i>
            </h3>
            <p class="text-xs text-gray-400 mt-0.5">Click any register button here to open the registration page and input your 10-digit number.</p>
          </div>
        </div>

        <!-- Step 2 -->
        <div class="card-glass rounded-xl p-3.5 flex items-start gap-3.5 border-l-4 border-l-amber-500">
          <div class="w-7 h-7 rounded-full bg-amber-500/20 text-amber-400 font-bold flex items-center justify-center text-xs flex-shrink-0 mt-0.5">
            2
          </div>
          <div>
            <h3 class="font-semibold text-sm text-gray-100">Set a Secure Password</h3>
            <p class="text-xs text-gray-400 mt-0.5">Create a strong password (letters & numbers) and confirm it for login security.</p>
          </div>
        </div>

        <!-- Step 3 -->
        <div class="card-glass rounded-xl p-3.5 flex items-start gap-3.5 border-l-4 border-l-emerald-500">
          <div class="w-7 h-7 rounded-full bg-emerald-500/20 text-emerald-400 font-bold flex items-center justify-center text-xs flex-shrink-0 mt-0.5">
            3
          </div>
          <div>
            <h3 class="font-semibold text-sm text-gray-100">Confirm Code & Start</h3>
            <p class="text-xs text-gray-400 mt-0.5">Verify invitation code <span class="text-amber-300 font-mono font-medium">1kuV2648127</span> is filled in, submit, and claim your rewards.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Key Platform Features -->
    <section class="w-full mt-10">
      <div class="flex items-center gap-2 mb-4">
        <i data-lucide="shield-check" class="w-5 h-5 text-gold-400"></i>
        <h2 class="font-display font-bold text-lg text-white">Why Register with Our Code?</h2>
      </div>

      <div class="grid grid-cols-1 gap-3">
        <div class="bg-brandDark-800/80 rounded-xl p-4 border border-gray-800 flex items-center gap-3.5">
          <div class="p-2.5 rounded-lg bg-amber-500/10 text-amber-400 flex-shrink-0">
            <i data-lucide="zap" class="w-5 h-5"></i>
          </div>
          <div>
            <h4 class="font-medium text-sm text-white">Instant UPI Withdrawals</h4>
            <p class="text-xs text-gray-400 mt-0.5">Seamless payout processing directly to your preferred bank account or UPI ID.</p>
          </div>
        </div>

        <div class="bg-brandDark-800/80 rounded-xl p-4 border border-gray-800 flex items-center gap-3.5">
          <div class="p-2.5 rounded-lg bg-emerald-500/10 text-emerald-400 flex-shrink-0">
            <i data-lucide="gift" class="w-5 h-5"></i>
          </div>
          <div>
            <h4 class="font-medium text-sm text-white">VIP Daily Check-In Bonus</h4>
            <p class="text-xs text-gray-400 mt-0.5">Unlock consecutive log-in rewards, rebate commissions, and extra perks.</p>
          </div>
        </div>

        <div class="bg-brandDark-800/80 rounded-xl p-4 border border-gray-800 flex items-center gap-3.5">
          <div class="p-2.5 rounded-lg bg-blue-500/10 text-blue-400 flex-shrink-0">
            <i data-lucide="headphones" class="w-5 h-5"></i>
          </div>
          <div>
            <h4 class="font-medium text-sm text-white">Dedicated 24/7 Support</h4>
            <p class="text-xs text-gray-400 mt-0.5">Instant live chat assistance on official support channels round the clock.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="w-full mt-10">
      <div class="flex items-center gap-2 mb-4">
        <i data-lucide="help-circle" class="w-5 h-5 text-gold-400"></i>
        <h2 class="font-display font-bold text-lg text-white">Frequently Asked Questions</h2>
      </div>

      <div class="space-y-2.5" id="faqAccordion">
        <!-- FAQ 1 -->
        <div class="card-glass rounded-xl overflow-hidden">
          <button 
            type="button" 
            onclick="toggleFaq(1)" 
            class="w-full px-4 py-3 text-left flex items-center justify-between text-sm font-semibold text-gray-200 hover:text-white"
          >
            <span>What is the official BDG invitation code?</span>
            <i id="faq-icon-1" data-lucide="chevron-down" class="w-4 h-4 transition-transform text-gold-400"></i>
          </button>
          <div id="faq-ans-1" class="hidden px-4 pb-3.5 pt-0 text-xs text-gray-400 leading-relaxed border-t border-gray-800/60 mt-1">
            The official referral invitation code is <strong class="text-amber-300 font-mono">1kuV2648127</strong>. Using this ensures you receive all eligible new-user rewards and referral benefits.
          </div>
        </div>

        <!-- FAQ 2 -->
        <div class="card-glass rounded-xl overflow-hidden">
          <button 
            type="button" 
            onclick="toggleFaq(2)" 
            class="w-full px-4 py-3 text-left flex items-center justify-between text-sm font-semibold text-gray-200 hover:text-white"
          >
            <span>How long does registration take?</span>
            <i id="faq-icon-2" data-lucide="chevron-down" class="w-4 h-4 transition-transform text-gold-400"></i>
          </button>
          <div id="faq-ans-2" class="hidden px-4 pb-3.5 pt-0 text-xs text-gray-400 leading-relaxed border-t border-gray-800/60 mt-1">
            The registration process takes under 1 minute. All you need is your mobile number and a password to start playing immediately.
          </div>
        </div>

        <!-- FAQ 3 -->
        <div class="card-glass rounded-xl overflow-hidden">
          <button 
            type="button" 
            onclick="toggleFaq(3)" 
            class="w-full px-4 py-3 text-left flex items-center justify-between text-sm font-semibold text-gray-200 hover:text-white"
          >
            <span>What do I do if the code doesn't appear?</span>
            <i id="faq-icon-3" data-lucide="chevron-down" class="w-4 h-4 transition-transform text-gold-400"></i>
          </button>
          <div id="faq-ans-3" class="hidden px-4 pb-3.5 pt-0 text-xs text-gray-400 leading-relaxed border-t border-gray-800/60 mt-1">
            If the code box is blank, simply tap the <strong class="text-gray-300">Copy</strong> button on this page and paste <code class="text-amber-300">1kuV2648127</code> directly into the invitation code box on the registration screen.
          </div>
        </div>
      </div>
    </section>

    <!-- Bottom Secondary CTA -->
    <div class="w-full mt-8">
      <a 
        href="https://bdg4.vip//#/register?invitationCode=1kuV2648127" 
        target="_blank" 
        rel="noopener noreferrer"
        onclick="trackAndOpen(event)"
        class="w-full py-4 px-4 rounded-xl bg-gradient-to-r from-amber-500 to-yellow-500 text-gray-950 font-bold text-center flex items-center justify-center gap-2 shadow-lg active:scale-95 transition-all text-sm cursor-pointer"
      >
        <i data-lucide="sparkles" class="w-4 h-4 text-black"></i>
        <span>Go to Official BDG Registration</span>
      </a>
    </div>

    <!-- Legal & Risk Disclaimer Footer -->
    <footer class="w-full mt-10 pt-6 border-t border-gray-800/80 text-center">
      <div class="flex items-center justify-center gap-2 mb-2 text-rose-400 font-semibold text-xs">
        <span class="border border-rose-500/50 bg-rose-950/40 px-2 py-0.5 rounded text-[10px] tracking-wider uppercase font-bold">18+ ONLY</span>
        <span>Financial Risk Disclaimer</span>
      </div>
      <p class="text-[11px] text-gray-400 leading-relaxed max-w-sm mx-auto">
        This game involves an element of financial risk and may be addictive. Please play responsibly and at your own risk. This is an informational promo page intended solely for adult users in regions where permitted by law.
      </p>
      <p class="text-[10px] text-gray-400 mt-3">
        © 2026 Promo Partner Portal. All rights reserved.
      </p>
    </footer>

  </main>

  <!-- Vanilla JavaScript Logic -->
  <script>
    // Exact destination URL with invitation code
    const TARGET_URL = "https://bdg4.vip//#/register?invitationCode=1kuV2648127";

    // Global launcher that reliably opens the link in new tab or redirects
    function openTargetUrl() {
      const opened = window.open(TARGET_URL, '_blank', 'noopener,noreferrer');
      if (!opened) {
        window.location.href = TARGET_URL;
      }
    }

    function trackAndOpen(e) {
      if (e) {
        // Let standard anchor behavior proceed or trigger openTargetUrl if prevented
        return true;
      }
    }

    // Initialize Lucide icons
    lucide.createIcons();

    // Copy to clipboard with fallback and toast feedback
    function copyInvitationCode() {
      const codeInput = document.getElementById('inviteCode');
      const textToCopy = codeInput.value;

      try {
        codeInput.select();
        codeInput.setSelectionRange(0, 99999); // For mobile devices
        
        // Use document.execCommand for iFrame and broader WebView support
        const successful = document.execCommand('copy');
        if (successful) {
          showToast();
        } else {
          // Fallback navigator API
          navigator.clipboard.writeText(textToCopy).then(() => {
            showToast();
          });
        }
      } catch (err) {
        try {
          navigator.clipboard.writeText(textToCopy).then(() => {
            showToast();
          });
        } catch (e) {
          console.error('Failed to copy', e);
        }
      }
    }

    // Toast handler
    let toastTimeout;
    function showToast() {
      const toast = document.getElementById('toast');
      clearTimeout(toastTimeout);
      
      toast.classList.remove('opacity-0', '-translate-y-5', 'pointer-events-none');
      toast.classList.add('opacity-100', 'translate-y-0');

      toastTimeout = setTimeout(() => {
        toast.classList.remove('opacity-100', 'translate-y-0');
        toast.classList.add('opacity-0', '-translate-y-5', 'pointer-events-none');
      }, 2500);
    }

    // Accordion toggle handler
    function toggleFaq(index) {
      const ans = document.getElementById(`faq-ans-${index}`);
      const icon = document.getElementById(`faq-icon-${index}`);
      const isHidden = ans.classList.contains('hidden');

      // Close all first for neat accordion effect
      [1, 2, 3].forEach(i => {
        const otherAns = document.getElementById(`faq-ans-${i}`);
        const otherIcon = document.getElementById(`faq-icon-${i}`);
        if (otherAns && otherIcon) {
          otherAns.classList.add('hidden');
          otherIcon.classList.remove('rotate-180');
        }
      });

      if (isHidden) {
        ans.classList.remove('hidden');
        icon.classList.add('rotate-180');
      }
    }
  </script>
</body>
</html>