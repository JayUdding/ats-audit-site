---
layout: default
title: FAQ — StoicResume
permalink: /faq/
---

<div class="faq-container">
  <h1>Frequently Asked Questions</h1>
  <p class="faq-lead">Direct answers about the mechanics of the audit.</p>

  <div class="faq-section">
    <h2>About the Service & Methodology</h2>

    <div class="faq-item">
      <button class="faq-question">What exactly are you selling?</button>
      <div class="faq-answer">
        <p>An objective, forensic breakdown of your resume's ATS (Applicant Tracking System) compatibility. We do not give you a score or a meaningless percentage. We perform manual tests—like the Brutal Copy-Paste Test—inspect your file's structure, and tell you precisely what will break, why it will break, and how to fix it. Theory is good; verifiable evidence is better. But the process can be nuanced: We distinguish between:
        
- **Confirmed issues** — directly observed in the file or extracted text
- **Likely risks** — strongly suggested by symptoms, but not fully provable without the source document
- **Unknowns** — issues that cannot be responsibly claimed from the available evidence

This matters. We do not present guesses as facts. A real ATS review has multiple layers, and we separate them clearly</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">How are you different from a free ATS "scanner"?</button>
      <div class="faq-answer">
        <p>There are different kinds of ATS scanners,” and they are not all equal: they may miss file-level problems or overreport others. Most scanners simulate one parser and output a guess. They cannot see your file's underlying architecture—the tables, text boxes, or header/footer traps that cause actual parsing failures. ATS scanner usually do not reliably reveal real parser behavior, layout failure modes or true system-specific ingestion issues. Our audit is Human-in-the-Loop (HIL): a human reviewer performs the diagnostic tests that AI cannot execute, then uses AI to accelerate keyword analysis. The final judgment is human. We distinguish between what we can confirm and what is only likely. In sum: the actual ATS that will be used on your resume may: parse differently from your scanner; strip headers/footers; mishandle columns differently; handle Unicode differently; store fields differently or search differently later. So an ATS scanner can reveal some likely risks; some parsing symptoms; some keyword gaps; but not a universal verdict.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What is your "Human-in-the-Loop" (HIL) advantage?</button>
      <div class="faq-answer">
        <p>In short: the nuance that is needed. AI cannot [*reliably* in April 2026] open your file, press Ctrl+A, or visually confirm a text box. It cannot run the Brutal Copy-Paste Test and interpret the scrambled output. The AI prompt is a content and text-level analysis tool. It works on whatever text you give it. It cannot see the original file. It cannot see invisible formatting. Our advantage is simple: we perform the manual, mechanical tests that are still required for a reliable audit. From a PDF file it cannot determine whether the original source file used tables or text boxes; whether the PDF was created via Save As or Print to PDF (though sometimes it can infer it if the text layer is absent or garbled); whether headers/footers in the original Word file contained critical data; or whether multi-column layout existed in the source document. AI assists; the human verifies. This prevents the false certainty that pure automation sells.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>The Process & What We Need</h2>

    <div class="faq-item">
      <button class="faq-question">What is the "Brutal Copy-Paste Test"?</button>
      <div class="faq-answer">
        <p>**The first and most critical test—a strong first-pass validation step**. It is best understood as a first-line extraction sanity test that answers one question: when the text is pulled out of the file, does it remain clean, linear, complete, and intelligible? If the answer is no:
you already have a serious ATS risk. If the answer is yes: that is good but it does not prove universal ATS safety because it does not prove that there are no text boxes, tables, headers/footers, that every ATS will parse it correctly or that every field will be mapped correct, or that the original was structurally cleean. So the Brutal Copy-Paste Test is necessary and useful but not sufficient on its own. 

 
**This is how it works**: we manually copy all text from your resume file and paste it into a plain-text editor. If the output is scrambled, out of order, or missing data (contact info, dates), your resume will fail in an ATS. This is a mechanical reality, not an opinion. We perform it on every audit.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Do you need my original Word file (.DOCX), or is a PDF enough?</button>
      <div class="faq-answer">
        <p>Ideally, yes; because while a PDF tells you what survives export and extraction but does not always tell you how the source was built because PDF export can flatten or normalize some underlying problems. In practice a PDF is often sufficient for a strong audit—a final PDF plus copy-paste test can catch a lot. We can assess text extraction, keyword gaps, and visible structure. However, if you provide the source .DOCX, we can also inspect the document architecture for hidden risks—tables, text boxes, headers/footers. We will never claim to confirm something we cannot see. The .DOCX provides the highest confidence how the source was built. So the precise answer is: you do NOT always need the source document to identify risk. But: You DO need the source document to confirm many structural causes. That is the clean distinction.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Why can't I just upload a screenshot?</button>
      <div class="faq-answer">
        <p>**A screenshot is not enough for ATS analysis.** A screenshot shows only visual appearance and visual appearance alone is **insufficient**. An ATS is a text extraction engine, not a pair of eyes. We need the actual file to test how the machine-readable text layer behaves. Images reveal nothing about parsing. When you upload an image or screenshot of a resume to an AI the AI reads the image visually using computer vision; it sees what the resume looks like but
 it cannot read the underlying text structure; it cannot detect encoding issues nor detect invisible formatting problems.
It will essentially describe what it sees visually, not what an ATS parser would extract</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What do you check against the job description?</button>
      <div class="faq-answer">
        <p>We perform a keyword alignment analysis: we compare your resume's wording against the target job description to identify exact matches, critical missing terms, acronym mismatches, and skills that are implied but not explicitly stated. This is not "keyword stuffing"—it is aligning your truthful experience with the language a recruiter's Boolean search will use.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>Technical & ATS Details</h2>

    <div class="faq-item">
      <button class="faq-question">Can you guarantee my resume will pass every ATS?</button>
      <div class="faq-answer">
        <p>No. Anyone who guarantees universal compatibility is lying. There is no universal standard. We provide a forensic review based on defensive best practices and file-level testing. We significantly increase your probability of passing through the vast majority of systems by eliminating the most common, proven failure points.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What are the most common failures you find?</button>
      <div class="faq-answer">
        <p>In order of frequency:</p>
        <ol>
          <li>The Image-Only PDF (created via "Print to PDF," text is not selectable).</li>
          <li>The Table Trap (using tables for layout, which scrambles reading order).</li>
          <li>The Header Graveyard (placing contact info in Word headers/footers, which are stripped).</li>
          <li>The Column Bleed (multi-column layouts that concatenate text into gibberish).</li>
          <li>The Pipe Misuse (using the pipe character | inside bullet points or skills lists).</li>
        </ol>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">I used a Canva/Google Docs template. Is that risky?</button>
      <div class="faq-answer">
        <p>Often, yes. Visually appealing templates frequently rely on multi-column layouts, sidebars, and floating text boxes for design. These are parsing hazards. We test the actual file you plan to submit and will flag any observed extraction issues.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>AI vs. Human Review</h2>

    <div class="faq-item">
      <button class="faq-question">How does AI fit into your process?</button>
      <div class="faq-answer">
        <p>AI is our acceleration layer and is *complementary* to the HIL audit **but never an autonomous reviewer**. It quickly compares your resume text to the job description, identifies keyword gaps, spots weak bullets, and suggests concise rewrites. This allows our human reviewer to focus on the tasks AI cannot yet do reliably today considering the ATS parser methods that are actually being used: file structure inspection, extraction testing, *and, most importantly* provide nuanced judgment of the AI assessment itself: guarding against overreach, missed nuance or inflated claims. In sum: AI does not replace human judgment and does not provide magic structural certainty.**</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Can't I just use an AI myself?</button>
      <div class="faq-answer">
        <p>You can, and it might help. Depending on the robustness of the AI platform/model/tool used: a *good and sufficiently detailed* AI prompt (such as the one on our site that explicitly instructs it to not "hedge") an AI tool can assist and detect many text-level risks and keyword gaps, but it cannot confirm hidden file-level issues from pasted text alone and cannot be  fully trusted on its own today for a professional ATS forensic audit. 
        
        AI alone cannot:</p>
        <ul>
          <li>Run the Brutal Copy-Paste Test on your actual file.</li>
          <li>Determine if your PDF has a selectable text layer or is an image.</li>
          <li>Inspect a .DOCX for hidden tables or text boxes.</li>
          <li>Distinguish between a confirmed issue and a likely risk.</li>
          <li>Exercise judgment on what is truthful or appropriate for your specific career path.</li>
        </ul>
        <p>Our value is the synthesis and a layered approach: human verification augmented by AI efficiency.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>What You'll Receive & Timing</h2>

    <div class="faq-item">
      <button class="faq-question">What's in the audit report?</button>
      <div class="faq-answer">
        <p>A clear, actionable document containing:</p>
        <ul>
          <li><strong>Overall Assessment:</strong> High/Medium/Low ATS compatibility.</li>
          <li><strong>Confirmed Issues:</strong> Directly observed failures (e.g., "Text box found containing your name.").</li>
          <li><strong>Likely Risks:</strong> Problems inferred from symptoms, with explanations.</li>
          <li><strong>Keyword Alignment Summary:</strong> Matched and missing terms vs. your target job.</li>
          <li><strong>Weak Bullets:</strong> Specific lines with suggested rewrites.</li>
          <li><strong>Prioritized Fix List:</strong> Exact, line-by-line corrections.</li>
        </ul>
        <p>No flattery. No filler.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Do you rewrite my entire resume?</button>
      <div class="faq-answer">
        <p>No. We provide targeted edits, rewrites for weak sections, and structural recommendations. You remain the author; we act as your technical editor and ATS mechanic.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What is your turnaround time?</button>
      <div class="faq-answer">
        <p><strong>24 hours.</strong> We deliver the full audit report within one business day of receiving your resume and job description.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What do you need from me?</button>
      <div class="faq-answer">
        <p>Three things:</p>
        <ol>
          <li>Your current resume (PDF or .DOCX).</li>
          <li>The job description you're targeting.</li>
          <li>The email address you used for payment (or your Bitcoin transaction ID).</li>
        </ol>
        <p>Send them to <strong>audit@stoicresume.com</strong> after payment.</p>
      </div>
    </div>
  </div>

  <div class="faq-section">
    <h2>Pricing & Guarantee</h2>

    <div class="faq-item">
      <button class="faq-question">How much does it cost?</button>
      <div class="faq-answer">
        <p>The full forensic audit is <strong>\$20 USD</strong>. Given the manual, HIL work involved, this is likely underpriced. The price may increase.</p>
        <p>You may also pay with Bitcoin for a 50% discount (\$10 USD equivalent).</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What is your refund policy?</button>
      <div class="faq-answer">
        <p><strong>7-Day Refund. No questions asked.</strong> If the audit does not meet your expectations, email us within 7 days of delivery for a full refund.</p>
      </div>
    </div>

    <div class="faq-item">
      <button class="faq-question">What is your privacy policy?</button>
      <div class="faq-answer">
        <p>Your resume and email are permanently deleted from our systems 7 days after we deliver your audit report. We do not retain, sell, or share your data.</p>
      </div>
    </div>
  </div>

  <div class="faq-cta">
    <p><strong>The Choice</strong><br>
    Use the <a href="./free-prompt.html">free prompt</a> if you trust your own judgment.<br>
    Use the <a href="#order">audit</a> if you want an objective verdict.</p>
    <p><em>As Epictetus observed: "It is impossible for a man to learn what he thinks he already knows."</em></p>
  </div>

</div>

<style>
.faq-container {
  max-width: 800px;
  margin: 3rem auto;
  padding: 0 20px;
  font-family: Arial, sans-serif;
  color: #333;
}
.faq-lead {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 3rem;
  border-left: 3px solid #2c6c75;
  padding-left: 15px;
}
.faq-section {
  margin-bottom: 3rem;
}
.faq-section h2 {
  color: #2c6c75;
  border-bottom: 1px solid #eaeaea;
  padding-bottom: 10px;
  margin-bottom: 1.5rem;
}
.faq-item {
  margin-bottom: 1rem;
  border: 1px solid #eaeaea;
  border-radius: 6px;
  overflow: hidden;
}
.faq-question {
  width: 100%;
  padding: 18px 20px;
  text-align: left;
  font-weight: bold;
  font-size: 1rem;
  background-color: #f9f9f9;
  border: none;
  cursor: pointer;
  color: #2c6c75;
  transition: background-color 0.2s;
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
  font-size: 1.5rem;
  color: #777;
}
.faq-question.active::after {
  content: '-';
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
  max-height: 1000px;
}
.faq-answer p,
.faq-answer ul,
.faq-answer ol {
  margin-top: 0;
  line-height: 1.6;
}
.faq-answer ul,
.faq-answer ol {
  padding-left: 20px;
}
.faq-cta {
  margin-top: 4rem;
  padding: 2rem;
  background-color: #f9f9f9;
  border-radius: 8px;
  text-align: center;
  border: 1px solid #eaeaea;
}
.faq-cta p {
  margin-bottom: 1rem;
}
.faq-cta a {
  color: #2c6c75;
  font-weight: bold;
}
@media (max-width: 600px) {
  .faq-container {
    padding: 0 15px;
  }
  .faq-question {
    padding: 15px;
    font-size: 0.95rem;
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

      // Close all other open answers (optional accordion behavior)
      if (!isOpen) {
        document.querySelectorAll('.faq-answer.open').forEach(openAnswer => {
          openAnswer.classList.remove('open');
          openAnswer.previousElementSibling.classList.remove('active');
        });
      }

      // Toggle current
      this.classList.toggle('active');
      answer.classList.toggle('open');
    });
  });
});
</script>
