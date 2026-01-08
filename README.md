<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Velocore Digital — Buy Crypto with Cash, Cards & Wires</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
    * { margin: 0; padding: 0; box-sizing: border-box; }
    :root {
      --header: #6951FF;
      --card1: #FF5555;
      --card2: #63A1FF;
      --text: #474747;
      --background: #FFFFFF;
    }
    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--background);
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }
    .container { width: 90%; max-width: 1200px; margin: 0 auto; }
    nav {
      background: var(--header);
      padding: 1rem 0;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 1.25rem;
      font-weight: 700;
      color: white;
    }
    .logo-icon {
      width: 32px;
      height: 32px;
      background: white;
      border-radius: 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--header);
      font-weight: bold;
      font-size: 14px;
    }
    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
      align-items: center;
    }
    .nav-links a {
      color: rgba(255, 255, 255, 0.9);
      text-decoration: none;
      transition: color 0.3s;
      font-weight: 500;
    }
    .nav-links a:hover {
      color: white;
    }
    .btn {
      padding: 0.75rem 1.5rem;
      border-radius: 9999px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s ease;
      border: none;
      font-family: 'Inter', sans-serif;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      text-decoration: none;
    }
    .btn-primary {
      background: white;
      color: var(--header);
    }
    .btn-primary:hover {
      transform: scale(1.05);
      box-shadow: 0 4px 20px rgba(105, 81, 255, 0.3);
    }
    .hero {
      padding: 12rem 0 6rem;
      text-align: center;
      background: linear-gradient(135deg, #f8f9ff, #eef1ff);
    }
    .hero h1 {
      font-size: 2.5rem;
      font-weight: 800;
      margin-bottom: 1.5rem;
      line-height: 1.2;
      color: var(--header);
    }
    .hero h1 span {
      color: var(--card1);
    }
    .hero p {
      font-size: 1.125rem;
      color: var(--text);
      max-width: 700px;
      margin: 0 auto 2.5rem;
      opacity: 0.9;
    }
    .hero-buttons {
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
    }
    .section { padding: 5rem 0; }
    .section-title { text-align: center; margin-bottom: 3rem; }
    .section-title h2 {
      font-size: 2.25rem;
      font-weight: 700;
      margin-bottom: 1rem;
      color: var(--header);
    }
    .section-title p {
      color: var(--text);
      font-size: 1.125rem;
      opacity: 0.8;
    }
    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }
    .feature-card {
      background: white;
      border-radius: 16px;
      padding: 2rem;
      transition: all 0.3s ease;
      box-shadow: 0 4px 20px rgba(0,0,0,0.08);
      border: 1px solid #eee;
    }
    .feature-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 30px rgba(0,0,0,0.15);
    }
    .feature-icon {
      width: 64px;
      height: 64px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1.5rem;
      font-size: 1.5rem;
      color: white;
    }
    .cash { background: var(--card1); }
    .card { background: var(--header); }
    .wire { background: var(--card2); }
    .feature-card h3 {
      font-size: 1.25rem;
      margin-bottom: 1rem;
      color: var(--text);
    }
    .feature-card p {
      color: var(--text);
      opacity: 0.8;
    }
    .steps-section { background: #f8f9ff; }
    .steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }
    .step {
      text-align: center;
      padding: 2rem;
      background: white;
      border-radius: 16px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    }
    .step-number {
      width: 64px;
      height: 64px;
      background: var(--header);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 1.5rem;
      font-size: 1.5rem;
      font-weight: 700;
      color: white;
    }
    .step h3 {
      font-size: 1.25rem;
      margin-bottom: 1rem;
      color: var(--text);
    }
    .step p {
      color: var(--text);
      opacity: 0.8;
    }
    .security { background: white; }
    .security-content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4rem;
      align-items: center;
    }
    .security-info h2 {
      font-size: 2.25rem;
      font-weight: 700;
      margin-bottom: 1.5rem;
      color: var(--header);
    }
    .security-info p {
      color: var(--text);
      opacity: 0.9;
      margin-bottom: 2rem;
      font-size: 1.125rem;
    }
    .security-item {
      display: flex;
      gap: 1rem;
      margin-bottom: 1.5rem;
    }
    .security-icon {
      width: 40px;
      height: 40px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      flex-shrink: 0;
    }
    .icon-compliance { background: var(--card1); }
    .icon-encryption { background: var(--header); }
    .icon-institutional { background: var(--card2); }
    .security-item h3 {
      font-size: 1.125rem;
      font-weight: 600;
      margin-bottom: 0.25rem;
      color: var(--text);
    }
    .security-item p {
      color: var(--text);
      opacity: 0.8;
      margin: 0;
    }
    .security-terminal {
      background: #f8f9ff;
      border-radius: 16px;
      padding: 2rem;
      border: 1px solid #eee;
    }
    .terminal-header {
      display: flex;
      justify-content: space-between;
      margin-bottom: 1.5rem;
    }
    .terminal-dots {
      display: flex;
      gap: 0.5rem;
    }
    .dot { width: 12px; height: 12px; border-radius: 50%; }
    .dot-red { background: var(--card1); }
    .dot-yellow { background: #eab308; }
    .dot-green { background: #22c55e; }
    .terminal-url {
      color: #666;
      font-size: 0.875rem;
    }
    .terminal-item {
      display: flex;
      justify-content: space-between;
      padding: 0.5rem 0;
      border-bottom: 1px solid #eee;
    }
    .terminal-item:last-child {
      border-bottom: none;
    }
    .terminal-check {
      color: #22c55e;
      font-weight: 600;
    }
    .cta-section {
      background: linear-gradient(135deg, var(--header), #8a7bff);
      color: white;
      text-align: center;
      padding: 5rem 0;
    }
    .cta h2 {
      font-size: 2.25rem;
      margin-bottom: 1.5rem;
    }
    .cta p {
      max-width: 600px;
      margin: 0 auto 2.5rem;
      font-size: 1.125rem;
      opacity: 0.9;
    }
    footer {
      background: #f8f9ff;
      padding: 4rem 0 2rem;
      border-top: 1px solid #eee;
    }
    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      margin-bottom: 3rem;
    }
    .footer-col h3 {
      font-size: 1.125rem;
      margin-bottom: 1.5rem;
      font-weight: 600;
      color: var(--header);
    }
    .footer-col ul {
      list-style: none;
    }
    .footer-col ul li {
      margin-bottom: 0.75rem;
    }
    .footer-col ul li a {
      color: var(--text);
      text-decoration: none;
      transition: color 0.3s;
      opacity: 0.8;
    }
    .footer-col ul li a:hover {
      color: var(--header);
      opacity: 1;
    }
    .copyright {
      text-align: center;
      padding-top: 2rem;
      border-top: 1px solid #eee;
      color: var(--text);
      font-size: 0.875rem;
      opacity: 0.7;
    }

    /* Mobile Responsive */
    @media (max-width: 768px) {
      .nav-links {
        display: none;
      }
      
      /* Always show Get Started on mobile */
      .get-started-mobile {
        display: block !important;
      }
      
      .hero h1 {
        font-size: 2rem;
      }
      
      .security-content {
        grid-template-columns: 1fr;
        gap: 2rem;
      }
      
      .steps {
        grid-template-columns: 1fr;
      }
      
      .steps .step {
        padding: 1.5rem;
      }
    }
    
    @media (min-width: 769px) {
      .get-started-mobile {
        display: none !important;
      }
    }
  </style>
</head>
<body>
  <nav>
    <div class="container nav-container">
      <div class="logo">
        <div class="logo-icon">VD</div>
        <span>Velocore Digital</span>
      </div>
      
      <!-- Desktop: Full nav + Get Started -->
      <div style="display: flex; align-items: center; gap: 2rem;">
        <ul class="nav-links">
          <li><a href="#features">Features</a></li>
          <li><a href="#how-it-works">How It Works</a></li>
          <li><a href="#security">Security</a></li>
        </ul>
        <a href="get-started.html" class="btn btn-primary">Get Started</a>
      </div>
      
      <!-- Mobile: Only Get Started button -->
      <a href="get-started.html" class="btn btn-primary get-started-mobile" style="margin-left: auto;">Get Started</a>
    </div>
  </nav>

  <section class="hero">
    <div class="container">
      <h1>The Most Reliable Way to <span>Buy Crypto</span></h1>
      <p>Purchase cryptocurrency instantly with cash, cards, or wire transfers through our secure, compliant infrastructure designed for institutions and individuals alike.</p>
      <div class="hero-buttons">
        <a href="get-started.html" class="btn btn-primary">Start Trading Now <i class="fas fa-arrow-right" style="margin-left: 8px;"></i></a>
        <a href="demo.html" class="btn btn-demo">View Demo</a>
      </div>
    </div>
  </section>

  <!-- Rest of the page content remains the same -->
  <section id="features" class="section">
    <div class="container">
      <div class="section-title">
        <h2>Seamless Payment Methods</h2>
        <p>Choose the payment method that works best for you</p>
      </div>
      <div class="features-grid">
        <div class="feature-card">
          <div class="feature-icon cash"><i class="fas fa-dollar-sign"></i></div>
          <h3>Cash Deposits</h3>
          <p>Deposit cash at thousands of partner locations nationwide. Instant crypto delivery to your wallet.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon card"><i class="fas fa-credit-card"></i></div>
          <h3>Card Payments</h3>
          <p>Buy crypto instantly with debit or credit cards. Industry-leading security and fraud protection.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon wire"><i class="fas fa-globe-americas"></i></div>
          <h3>Wire Transfers</h3>
          <p>High-volume purchases with bank wires. Perfect for institutional investors and large transactions.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="how-it-works" class="section steps-section">
    <div class="container">
      <div class="section-title">
        <h2>How Velocore Digital Works</h2>
        <p>Simple, secure, and lightning fast</p>
      </div>
      <div class="steps">
        <div class="step">
          <div class="step-number">1</div>
          <h3>Choose Your Method</h3>
          <p>Select cash, card, or wire transfer based on your preference and transaction size.</p>
        </div>
        <div class="step">
          <div class="step-number">2</div>
          <h3>Verify Identity</h3>
          <p>Complete our quick and secure KYC process to comply with regulatory requirements.</p>
        </div>
        <div class="step">
          <div class="step-number">3</div>
          <h3>Make Payment</h3>
          <p>Complete your payment using your chosen method with real-time processing.</p>
        </div>
        <div class="step">
          <div class="step-number">4</div>
          <h3>Receive Crypto</h3>
          <p>Your cryptocurrency is delivered instantly to your wallet with full transaction transparency.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="security" class="section security">
    <div class="container">
      <div class="security-content">
        <div class="security-info">
          <h2>Bank-Grade Security</h2>
          <p>Your security is our top priority. We implement military-grade encryption, multi-factor authentication, and cold storage solutions to protect your assets.</p>
          <div>
            <div class="security-item">
              <div class="security-icon icon-compliance"><i class="fas fa-shield-alt"></i></div>
              <div><h3>Regulatory Compliance</h3><p>Fully licensed and compliant with AML/KYC regulations in all operating jurisdictions.</p></div>
            </div>
            <div class="security-item">
              <div class="security-icon icon-encryption"><i class="fas fa-lock"></i></div>
              <div><h3>Advanced Encryption</h3><p>End-to-end encryption protects your data and transactions at every step.</p></div>
            </div>
            <div class="security-item">
              <div class="security-icon icon-institutional"><i class="fas fa-users"></i></div>
              <div><h3>Institutional Grade</h3><p>Trusted by financial institutions, hedge funds, and high-net-worth individuals worldwide.</p></div>
            </div>
          </div>
        </div>
        <div class="security-terminal">
          <div class="terminal-header">
            <div class="terminal-dots">
              <div class="dot dot-red"></div>
              <div class="dot dot-yellow"></div>
              <div class="dot dot-green"></div>
            </div>
            <div class="terminal-url">velocoredigital.com/security</div>
          </div>
          <div class="terminal-item"><span>SSL Certificate</span><span class="terminal-check">✓ Valid</span></div>
          <div class="terminal-item"><span>2FA Enabled</span><span class="terminal-check">✓ Active</span></div>
          <div class="terminal-item"><span>Cold Storage</span><span class="terminal-check">✓ 98% Secured</span></div>
          <div class="terminal-item"><span>Audit Status</span><span class="terminal-check">✓ Quarterly</span></div>
        </div>
      </div>
    </div>
  </section>

  <section class="cta-section">
    <div class="container cta">
      <h2>Ready to Start Your Crypto Journey?</h2>
      <p>Join thousands of satisfied users who trust Velocore Digital for their cryptocurrency purchases. Get started in minutes.</p>
      <div class="hero-buttons">
        <a href="get-started.html" class="btn btn-primary">Create Account</a>
        <a href="contact-sales.html" class="btn btn-demo">Contact Sales</a>
      </div>
    </div>
  </section>

  <footer>
    <div class="container">
      <div class="footer-grid">
        <div class="footer-col">
          <div class="logo" style="margin-bottom: 1.5rem; color: var(--header);">
            <div class="logo-icon">VD</div>
            <span>Velocore Digital</span>
          </div>
          <p style="color: var(--text); opacity: 0.8;">Building the most reliable infrastructure for purchasing cryptocurrency.</p>
        </div>
        <div class="footer-col">
          <h3>Products</h3>
          <ul>
            <li><a href="#">Cash Purchases</a></li>
            <li><a href="#">Card Processing</a></li>
            <li><a href="#">Wire Transfers</a></li>
            <li><a href="#">API Integration</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h3>Company</h3>
          <ul>
            <li><a href="#">About Us</a></li>
            <li><a href="#">Careers</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h3>Legal</h3>
          <ul>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Terms of Service</a></li>
            <li><a href="#">Compliance</a></li>
            <li><a href="#">Licenses</a></li>
          </ul>
        </div>
      </div>
      <div class="copyright">&copy; 2025 Velocore Digital. All rights reserved. Licensed and regulated in accordance with applicable laws.</div>
    </div>
  </footer>

  <script>
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          window.scrollTo({ top: target.offsetTop - 80, behavior: 'smooth' });
        }
      });
    });
  </script>
</body>
</html>

