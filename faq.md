---
layout: default
title: FAQ — StoicResume
permalink: /faq/
---

<div class="faq-container">
  <h1>Frequently Asked Questions</h1>
  <p class="faq-lead">Direct answers about the mechanics of the audit.</p>

  <div class="faq-section">
    <h2>About the Service &amp; Methodology</h2>

    <div class="faq-item">
      <button class="faq-question">What exactly are you selling?</button>
      <div class="faq-answer">
        <p>An objective, forensic breakdown of your resume’s ATS (Applicant Tracking System) compatibility.</p>
        <p>We do <strong>not</strong> give you a vanity score or a meaningless percentage. We perform manual tests, such as the <strong>Brutal Copy-Paste Test</strong>, inspect your file’s structure, and tell you precisely what will break, why it will break, and how to fix it.</p>
        <p>Theory is good. Verifiable evidence is better.</p>
        <p>Because the process can be nuanced, we distinguish between:</p>
        <ul>
          <li><strong>Confirmed issues</strong> — directly observed in the file or extracted text</li>
          <li><strong>Likely risks</strong> — strongly suggested by symptoms, but not fully provable without the source document</li>
          <li><strong>Unknowns</strong> — issues that cannot be responsibly claimed from the available evidence</li>
        </ul>
        <p>This matters. We do not present guesses as facts. A real ATS review has multiple layers, and we separate them clearly.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">How are you different from a free ATS “scanner”?</button>
      <div class="faq-answer">
        <p>There are different kinds of ATS scanners, and they are not all equal.</p>
        <p>Most scanners simulate one parser and output a guess. They may miss file-level problems or overreport others. They usually cannot see your file’s underlying architecture — tables, text boxes, or header/footer traps — that cause real parsing failures.</p>
        <p>Most ATS scanners do <strong>not</strong> reliably reveal actual parser behavior, layout failure modes, or system-specific ingestion issues.</p>
        <p>Our audit is <strong>Human-in-the-Loop (HIL)</strong>: a human reviewer performs the diagnostic tests that AI cannot execute, then uses AI to accelerate keyword analysis. The final judgment is human.</p>
        <p>We also distinguish between what we can confirm and what is only likely.</p>
        <p>In short, the actual ATS used on your resume may:</p>
        <ul>
          <li>parse differently from your scanner</li>
          <li>strip headers or footers</li>
          <li>mishandle columns</li>
          <li>handle Unicode differently</li>
          <li>store fields differently</li>
          <li>search differently later</li>
        </ul>
        <p>So a scanner can reveal some likely risks and keyword gaps, but it cannot deliver a universal verdict.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What is your “Human-in-the-Loop” (HIL) advantage?</button>
      <div class="faq-answer">
        <p>In short: nuance.</p>
        <p>AI cannot reliably open your file, press Ctrl+A, or visually confirm a text box. It cannot run the Brutal Copy-Paste Test and interpret scrambled output with confidence.</p>
        <p>AI is a content- and text-level analysis tool. It works on whatever text you give it. It cannot truly inspect the original file structure or invisible formatting.</p>
        <p>Our advantage is simple: we perform the manual, mechanical tests still required for a reliable audit.</p>
        <p>For example, from a PDF alone, AI cannot reliably determine:</p>
        <ul>
          <li>whether the original file used tables or text boxes</li>
          <li>whether the PDF was created via “Save As” or “Print to PDF”</li>
          <li>whether headers or footers in the original Word file contained critical data</li>
          <li>whether the source document used a multi-column layout</li>
        </ul>
        <p>AI assists. The human verifies. That is what prevents the false certainty that pure automation often sells.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>The Process &amp; What We Need</h2>

    <div class="faq-item">
      <button class="faq-question">What is the “Brutal Copy-Paste Test”?</button>
      <div class="faq-answer">
        <p><strong>The first and most critical test — a strong first-pass validation step.</strong></p>
        <p>It is best understood as a first-line extraction sanity test that answers one question:</p>
        <p><strong>When the text is pulled out of the file, does it remain clean, linear, complete, and intelligible?</strong></p>
        <p>If the answer is no, you already have a serious ATS risk.</p>
        <p>If the answer is yes, that is good — but it does <strong>not</strong> prove universal ATS safety. It does not prove that there are no text boxes, tables, or header/footer issues. It does not prove every ATS will parse it correctly, or that every field will be mapped correctly.</p>
        <p>So the Brutal Copy-Paste Test is necessary and useful, but not sufficient on its own.</p>
        <p><strong>This is how it works:</strong> we manually copy all text from your resume file and paste it into a plain-text editor. If the output is scrambled, out of order, or missing data such as contact information or dates, your resume has a real ATS risk.</p>
        <p>This is a mechanical reality, not an opinion. We perform it on every audit.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Do you need my original Word file (.DOCX), or is a PDF enough?</button>
      <div class="faq-answer">
        <p>Ideally, yes — the original .DOCX gives us the highest confidence.</p>
        <p>A PDF tells us what survives export and extraction, but it does not always reveal how the source document was built. PDF export can flatten or normalize some underlying problems.</p>
        <p>In practice, a PDF is often sufficient for a strong audit. A final PDF plus extraction testing can catch a lot.</p>
        <p>However, if you provide the source .DOCX, we can also inspect the document architecture for hidden risks such as:</p>
        <ul>
          <li>tables</li>
          <li>text boxes</li>
          <li>headers and footers</li>
        </ul>
        <p>We will never claim to confirm something we cannot see.</p>
        <p>So the precise answer is:</p>
        <ul>
          <li>You do <strong>not</strong> always need the source document to identify risk.</li>
          <li>You <strong>do</strong> need the source document to confirm many structural causes.</li>
        </ul>
        <p>That is the clean distinction.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Why can’t I just upload a screenshot?</button>
      <div class="faq-answer">
        <p><strong>A screenshot is not enough for ATS analysis.</strong></p>
        <p>A screenshot shows only visual appearance, and visual appearance alone is insufficient. An ATS is a text extraction engine, not a pair of eyes.</p>
        <p>We need the actual file to test how the machine-readable text layer behaves. Images reveal nothing about parsing.</p>
        <p>When you upload an image or screenshot of a resume to an AI tool, the AI reads the image visually using computer vision. It sees what the resume looks like, but it cannot inspect the underlying text structure, detect encoding issues, or identify invisible formatting problems.</p>
        <p>It can describe what it sees visually. That is not the same as what an ATS parser will extract.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What do you check against the job description?</button>
      <div class="faq-answer">
        <p>We perform a keyword alignment analysis.</p>
        <p>We compare your resume’s wording against the target job description to identify:</p>
        <ul>
          <li>exact matches</li>
          <li>critical missing terms</li>
          <li>acronym mismatches</li>
          <li>skills that are implied but not explicitly stated</li>
        </ul>
        <p>This is not “keyword stuffing.” It is aligning your truthful experience with the language a recruiter’s Boolean search will use.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>Technical &amp; ATS Details</h2>

    <div class="faq-item">
      <button class="faq-question">Can you guarantee my resume will pass every ATS?</button>
      <div class="faq-answer">
        <p>No.</p>
        <p>Anyone who guarantees universal compatibility is lying. There is no universal standard.</p>
        <p>We provide a forensic review based on defensive best practices and file-level testing. We significantly improve your probability of passing through the vast majority of systems by eliminating the most common, proven failure points.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What are the most common failures you find?</button>
      <div class="faq-answer">
        <p>In rough order of frequency:</p>
        <ol>
          <li><strong>The Image-Only PDF</strong> — created via “Print to PDF”; text is not selectable.</li>
          <li><strong>The Table Trap</strong> — tables used for layout, scrambling reading order.</li>
          <li><strong>The Header Graveyard</strong> — contact information placed in headers or footers, which many systems strip.</li>
          <li><strong>The Column Bleed</strong> — multi-column layouts causing text to concatenate into gibberish.</li>
          <li><strong>The Pipe Misuse</strong> — using the pipe character (<code>|</code>) in ways that interfere with parsing clarity.</li>
        </ol>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">I used a Canva/Google Docs template. Is that risky?</button>
      <div class="faq-answer">
        <p>Often, yes.</p>
        <p>Visually appealing templates frequently rely on multi-column layouts, sidebars, and floating text boxes for design. These are common parsing hazards.</p>
        <p>We test the actual file you plan to submit and flag any observed extraction issues.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>AI vs. Human Review</h2>

    <div class="faq-item">
      <button class="faq-question">How does AI fit into your process?</button>
      <div class="faq-answer">
        <p>AI is our acceleration layer and is <em>complementary</em> to the HIL audit, <strong>but never an autonomous reviewer.</strong></p>
        <p>It quickly compares your resume text to the job description, identifies keyword gaps, spots weak bullets, and suggests concise rewrites.</p>
        <p>This allows our human reviewer to focus on the tasks AI still cannot do reliably today, including:</p>
        <ul>
          <li>file structure inspection</li>
          <li>extraction testing</li>
          <li>nuanced judgment of the AI’s own assessment</li>
        </ul>
        <p>That human judgment matters because it guards against overreach, missed nuance, and inflated claims.</p>
        <p>In short: AI does not replace human judgment, and it does not provide magical structural certainty.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Can’t I just use an AI myself?</button>
      <div class="faq-answer">
        <p>You can, and it may help.</p>
        <p>Depending on the quality of the model, platform, and prompt, AI can detect many text-level risks and keyword gaps. But it still cannot be fully trusted on its own for a professional ATS forensic audit.</p>
        <p>AI alone cannot:</p>
        <ul>
          <li>run the Brutal Copy-Paste Test on your actual file</li>
          <li>determine whether your PDF has a selectable text layer or is just an image</li>
          <li>inspect a .DOCX for hidden tables or text boxes</li>
          <li>distinguish between a confirmed issue and a likely risk</li>
          <li>exercise judgment about what is truthful or appropriate for your specific career path</li>
        </ul>
        <p>Our value is the synthesis: human verification, augmented by AI efficiency.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>What You’ll Receive &amp; Timing</h2>

    <div class="faq-item">
      <button class="faq-question">What’s in the audit report?</button>
      <div class="faq-answer">
        <p>A clear, actionable document containing:</p>
        <ul>
          <li><strong>Overall Assessment:</strong> High, Medium, or Low ATS compatibility</li>
          <li><strong>Confirmed Issues:</strong> directly observed failures</li>
          <li><strong>Likely Risks:</strong> inferred problems, with explanations</li>
          <li><strong>Keyword Alignment Summary:</strong> matched and missing terms versus your target job</li>
          <li><strong>Weak Bullets:</strong> specific lines with suggested rewrites</li>
          <li><strong>Prioritized Fix List:</strong> exact, line-by-line corrections</li>
        </ul>
        <p>No flattery. No filler.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Do you rewrite my entire resume?</button>
      <div class="faq-answer">
        <p>No.</p>
        <p>We provide targeted edits, rewrites for weak sections, and structural recommendations. You remain the author; we act as your technical editor and ATS mechanic.</p>
      </div>
    </div>
  </div>

  <a href="index.html" class="back-link">&larr; Back to StoicResume</a>

  <footer>
    &copy; 2026 StoicResume
  </footer>
</div>

<style>
  .faq-container {
    max-width: 800px;
    margin: 40px auto;
    padding: 0 20px;
    font-family: Arial, sans-serif;
    color: #333;
    font-size: 15px;
    line-height: 1.6;
  }

  .faq-container h1 {
    color: #2c6c75;
    font-size: 26px;
    margin-bottom: 5px;
  }

  .faq-container h2 {
    color: #2c6c75;
    font-size: 20px;
    margin-top: 30px;
  }

  .faq-lead {
    color: #555;
    margin-bottom: 30px;
  }

  .faq-section {
    margin-bottom: 35px;
  }

  .faq-item {
    margin-bottom: 12px;
    border: 1px solid #eaeaea;
    border-radius: 6px;
    overflow: hidden;
  }

  .faq-question {
    width: 100%;
    padding: 18px 20px;
    text-align: left;
    font-weight: bold;
    font-size: 15px;
    background-color: #f9f9f9;
    border: none;
    cursor: pointer;
    color: #2c6c75;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .faq-question:hover,
  .faq-question:focus {
    background-color: #f1f1f1;
  }

  .faq-question::after {
    content: '+';
    font-size: 22px;
    color: #777;
  }

  .faq-question.active::after {
    content: '−';
  }

  .faq-answer {
    padding: 0 20px;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease-out, padding 0.3s ease-out;
    background-color: #fff;
    border-top: 1px solid #f1f1f1;
  }

  .faq-answer.open {
    padding: 20px;
    max-height: 2000px;
  }

  .faq-answer p,
  .faq-answer ul,
  .faq-answer ol {
    margin-top: 0;
    margin-bottom: 14px;
  }

  .faq-answer ul,
  .faq-answer ol {
    padding-left: 22px;
  }

  .faq-answer code {
    font-family: Consolas, monospace;
    background: #f4f4f4;
    padding: 1px 4px;
    border-radius: 3px;
    font-size: 14px;
  }

  a {
    color: #2c6c75;
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  .back-link {
    display: inline-block;
    margin-top: 20px;
    margin-bottom: 20px;
    font-weight: bold;
    font-size: 14px;
  }

  footer {
    margin-top: 50px;
    padding-top: 20px;
    border-top: 1px solid #eaeaea;
    text-align: center;
    font-size: 13px;
    color: #666;
  }

  @media (max-width: 600px) {
    .faq-container {
      padding: 0 15px;
    }

    .faq-question {
      padding: 15px;
      font-size: 14px;
    }
  }
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const questions = document.querySelectorAll('.faq-question');

  questions.forEach(button => {
    button.addEventListener('click', function() {
      const answer = this.nextElementSibling;
      const isOpen = answer.classList.contains('open');

      if (!isOpen) {
        document.querySelectorAll('.faq-answer.open').forEach(openAnswer => {
          openAnswer.classList.remove('open');
          openAnswer.previousElementSibling.classList.remove('active');
        });
      }

      this.classList.toggle('active');
      answer.classList.toggle('open');
    });
  });
});
</script>
