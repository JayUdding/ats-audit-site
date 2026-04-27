
</div>
<!-- === MAIN CALL-TO-ACTION SECTION === -->
<div class="action-buttons-wrapper">

  <!-- 0. The Stripe/Fiat Button (Primary Purchase) -->
  <a href="YOUR_STRIPE_LINK_HERE" class="stripe-promo-btn">
    <div class="btn-main-text">
      <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24" style="vertical-align: middle; margin-right: 8px;"><path d="M20 4H4c-1.11 0-1.99.89-1.99 2L2 18c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V6c0-1.11-.89-2-2-2zm0 14H4v-6h16v6zm0-10H4V6h16v2z"/></svg>
      Order Full Audit — \$20
    </div>
    <div class="btn-sub-text">Secure checkout via Stripe</div>
  </a>

  <!-- 1. The Bitcoin Button (Discount Purchase) -->
  <a href="bitcoin:bc1qnrrvx2qp04mpq0jqmq0r59wwyn2qyw79c7plfl6akmxe3c4dnq5sjhjhm2?message=AuditATS" class="btc-promo-btn" id="btc-button" onclick="handleBitcoinClick(event)">
    <div class="btn-main-text">
      <img src="https://upload.wikimedia.org/wikipedia/commons/4/46/Bitcoin.svg" alt="Bitcoin Logo" width="20" height="20" style="vertical-align: middle; margin-right: 8px;">
      Order Full Audit — \$10 
    </div>
    <div class="btn-sub-text">Pay with Bitcoin & Save 50%</div>
  </a>

  <!-- 2. The Free Download Button (Secondary) -->
  <a href="./free-prompt.html" target="_blank" rel="noopener noreferrer" class="free-prompt-btn">
    <div class="btn-main-text">
      <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24" style="vertical-align: middle; margin-right: 8px;"><path d="M19 9h-4V3H9v6H5l7 7 7-7zM5 18v2h14v-2H5z"/></svg>
      Get the Free Prompt
    </div>
    <div class="btn-sub-text">Test your own resume in ChatGPT</div>
  </a>
</div>

<!-- === THE BITCOIN FALLBACK MODAL === -->
<div id="btc-modal" class="btc-modal">
  <div class="btc-modal-content">
    <span class="btc-modal-close" onclick="closeModal()">&times;</span>
    <h2 style="margin-top: 0; color: #1C2833;">Pay with Bitcoin</h2>
    <p>Please Send <strong>\$10 USD worth of Bitcoin</strong> to:</p>
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=bitcoin:bc1qnrrvx2qp04mpq0jqmq0r59wwyn2qyw79c7plfl6akmxe3c4dnq5sjhjhm2" alt="Bitcoin QR Code" style="margin: 15px 0;">
    <div class="btc-address-box">
      <code id="btc-address" style="font-size: 10px;">bc1qnrrvx2qp04mpq0jqmq0r59wwyn2qyw79c7plfl6akmxe3c4dnq5sjhjhm2</code>
      <button onclick="copyAddress()" class="copy-btn">Copy</button>
    </div>
    <p style="font-size: 13px; color: #666; margin-top: 15px;">
      After sending, email your resume + transaction ID to:<br>
      <strong style="color: #2E7D8C;">audit@stoicresume.com</strong>
    </p>
  </div>
</div>

<style>
  /* --- Layout Wrapper (The Fix: Added more bottom padding) --- */
  .action-buttons-wrapper {
    display: flex;
    flex-direction: row;         
    flex-wrap: wrap;             
    justify-content: center;     
    align-items: stretch;        
    gap: 25px;                   
    margin-top: 50px;            
    margin-bottom: 80px;         /* Increased margin */
    padding: 20px 20px 40px 20px; /* Extra 40px at bottom to prevent clipping */
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    box-sizing: border-box;
  }

  /* --- General Button Styles --- */
  .stripe-promo-btn, .btc-promo-btn, .free-prompt-btn {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    padding: 20px 24px;
    border-radius: 10px;
    transition: all 0.2s ease-in-out;
    width: 320px;                
    box-sizing: border-box;      /* Ensures border is included in width/height */
    text-align: center;
    margin-bottom: 10px;         /* Gives breathing room if buttons stack */
  }

  /* --- Stripe Button --- */
  .stripe-promo-btn {
    background-color: #2E7D8C;
    color: white !important;
    border: 2px solid #2E7D8C;
  }
  .stripe-promo-btn:hover {
    background-color: #245e69;
    transform: translateY(-3px);
    box-shadow: 0 8px 15px rgba(46, 125, 140, 0.2);
  }

  /* --- Bitcoin Button --- */
  .btc-promo-btn {
    background-color: #F7931A;
    color: white !important;
    border: 2px solid #F7931A;
  }
  .btc-promo-btn:hover {
    background-color: #e08316;
    transform: translateY(-3px);
    box-shadow: 0 8px 15px rgba(247, 147, 26, 0.2);
  }

  /* --- Free Prompt Button (The one in your screenshot) --- */
  .free-prompt-btn {
    background-color: #f0f7f8;   /* Very light teal tint for elegance */
    color: #2E7D8C !important;
    border: 2px solid #2E7D8C !important; /* Force the border to show */
  }
  .free-prompt-btn:hover {
    background-color: #ffffff;
    transform: translateY(-3px);
    box-shadow: 0 8px 15px rgba(46, 125, 140, 0.1);
  }

  .btn-main-text {
    font-size: 18px;
    font-weight: 600;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 4px;
  }

  .btn-sub-text, .free-btn-sub {
    font-size: 14px;
    font-weight: 400;
    opacity: 0.8;
  }

  /* --- Modal Styles --- */
  .btc-modal { display: none; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.7); }
  .btc-modal-content { background-color: #fff; padding: 30px; border-radius: 12px; text-align: center; max-width: 400px; margin: 10% auto; color: #333; }
  .btc-modal-close { float: right; font-size: 28px; font-weight: bold; cursor: pointer; }
  .btc-address-box { background-color: #f4f4f4; padding: 12px; border-radius: 6px; display: flex; justify-content: space-between; align-items: center; gap: 10px; margin-top: 10px; }
  .copy-btn { background-color: #F7931A; color: white; border: none; padding: 8px 14px; border-radius: 5px; cursor: pointer; font-weight: bold; }

  /* --- Mobile Responsiveness --- */
  @media (max-width: 700px) {
    .action-buttons-wrapper {
      flex-direction: column;      
      align-items: center;
    }
    .stripe-promo-btn, .btc-promo-btn, .free-prompt-btn {
      width: 100%;                 
      max-width: 320px;
    }
  }
</style>

<script>
  function handleBitcoinClick(event) {
    event.preventDefault(); // Prevents the link from firing immediately
    document.getElementById('btc-modal').style.display = 'block';
  }
  function closeModal() { document.getElementById('btc-modal').style.display = 'none'; }
  function copyAddress() {
    var address = document.getElementById('btc-address').innerText;
    navigator.clipboard.writeText(address);
    alert('Address copied!');
  }
  window.onclick = function(event) {
    if (event.target == document.getElementById('btc-modal')) { closeModal(); }
  }
</script>

<!-- === GLOBAL FOOTER === -->
<footer style="margin-top: 80px; padding: 40px 20px; border-top: 1px solid #ebedef; text-align: center; font-size: 13px; color: #666; line-height: 1.6;">
  <p>Questions or success stories? <a href="mailto:info@stoicresume.com" style="color: #2E7D8C; text-decoration: none; font-weight: 600;">info@stoicresume.com</a></p>
  <p style="opacity: 0.8;">
    &copy; 2026 StoicResume.com |
    <a href="/faq.html" class="footer-link">FAQ</a> |
    <a href="/privacy.html" class="footer-link">Privacy Policy</a> |
    <a href="/terms.html" class="footer-link">Terms of Service</a>
  </p>
</footer>
