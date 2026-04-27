---
layout: default
title: FAQ — StoicResume
permalink: /faq/
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FAQ - StoicResume</title>
  <style>
    body { 
      font-family: Arial, sans-serif; 
      line-height: 1.6; 
      color: #333; 
      max-width: 800px; 
      margin: 40px auto; 
      padding: 0 20px; 
      font-size: 15px; 
    }
    h1 { 
      color: #2c6c75; 
      font-size: 26px; 
      margin-bottom: 5px;
    }
    h2 { 
      color: #2c6c75; 
      font-size: 22px; 
      margin-top: 40px;
      border-bottom: 1px solid #eaeaea;
      padding-bottom: 5px;
    }
    h3 {
      color: #333;
      font-size: 16px;
      margin-top: 30px;
      margin-bottom: 10px;
    }
    p, ul, ol {
      margin-top: 0;
      margin-bottom: 15px;
    }
    ul, ol {
      padding-left: 20px;
    }
    a { color: #2c6c75; text-decoration: none; }
    a:hover { text-decoration: underline; }
    .back-link { display: inline-block; margin-bottom: 20px; font-weight: bold; font-size: 14px; }
    .faq-lead {
      color: #555;
      font-size: 16px;
      margin-bottom: 40px;
    }
  </style>
</head>
<body>

  <h1>Frequently Asked Questions</h1>
  <p class="faq-lead">Direct answers about the mechanics of our audit.</p>

  <h2>About the Service & Methodology</h2>

  <h3>What exactly are you selling?</h3>
  <p>An objective, forensic breakdown of your resume's ATS (Applicant Tracking System) compatibility. We do not give you a vanity score. We perform manual tests—like the Brutal Copy-Paste Test—inspect your file's structure, and tell you precisely what will break, why, and how to fix it.</p>
  <p>We separate our findings into clearly defined categories: <strong>Confirmed issues</strong> (directly observed), <strong>Likely risks</strong> (suggested by symptoms), and <strong>Unknowns</strong>. We do not present guesses as facts.</p>

  <h3>How are you different from a free ATS "scanner"?</h3>
  <p>Most scanners simulate <em>one</em> parser, guess the results, and miss critical file-level problems. They cannot see your file's underlying architecture—like hidden tables or text boxes—which are the actual causes of parsing failures.</p>
  <p>Our audit is Human-in-the-Loop (HIL). A human performs the diagnostic tests that AI cannot execute, then uses AI to accelerate keyword analysis. The final judgment is always human.</p>

  <h3>What is your "Human-in-the-Loop" advantage?</h3>
  <p>Nuance. AI cannot reliably open your file, press Ctrl+A, or visually confirm a floating text box. It cannot run the Brutal Copy-Paste Test and interpret scrambled output. AI assists with text analysis, but humans verify the actual file structure to prevent the false certainty that pure automation sells.</p>

  <h2>The Process & What We Need</h2>

  <h3>What is the "Brutal Copy-Paste Test"?</h3>
  <p>Our first and most critical sanity test. We manually copy all text from your resume file and paste it into a plain-text editor. If the output is scrambled, out of order, or missing contact data, your resume will fail in an ATS. This is a mechanical reality, not an opinion, and we perform it on every audit.</p>

  <h3>Do you need my original Word file (.DOCX), or is a PDF enough?</h3>
  <p>A PDF is often sufficient for a strong audit, as it allows us to test text extraction. However, providing the source .DOCX gives us the highest confidence, allowing us to inspect the document architecture for hidden risks like layout tables and header/footer traps.</p>

  <h3>Why can't I just upload a screenshot?</h3>
  <p>An ATS is a text extraction engine, not a pair of eyes. A screenshot only shows visual appearance. We need the actual file to test how the machine-readable text layer behaves.</p>

  <h3>What do you check against the job description?</h3>
  <p>We perform a keyword alignment analysis. We compare your resume against the target job to identify exact matches, missing terms, and acronym mismatches. This aligns your truthful experience with the language a recruiter's Boolean search will actually use.</p>

  <h2>Technical & ATS Details</h2>

  <h3>Can you guarantee my resume will pass every ATS?</h3>
  <p>No. Anyone who guarantees universal compatibility is lying because there is no universal standard. We eliminate the most common, proven failure points to dramatically increase your probability of passing through the vast majority of systems.</p>

  <h3>What are the most common failures you find?</h3>
  <ol>
    <li><strong>The Image-Only PDF:</strong> Created via "Print to PDF"; text is not selectable.</li>
    <li><strong>The Table Trap:</strong> Using tables for layout, which scrambles reading order.</li>
    <li><strong>The Header Graveyard:</strong> Placing contact info in Word headers, which are stripped.</li>
    <li><strong>The Column Bleed:</strong> Multi-column layouts that concatenate text into gibberish.</li>
    <li><strong>The Pipe Misuse:</strong> Overusing the pipe character (|) in ways that confuse parsers.</li>
  </ol>

  <h3>I used a Canva/Google Docs template. Is that risky?</h3>
  <p>Often, yes. Visually appealing templates frequently rely on multi-column layouts, sidebars, and floating text boxes for design. These are major parsing hazards.</p>

  <h2>AI vs. Human Review</h2>

  <h3>How does AI fit into your process?</h3>
  <p>AI is our acceleration layer, never an autonomous reviewer. It quickly spots keyword gaps, identifies weak bullets, and suggests concise rewrites. This allows our human reviewer to focus on file structure inspection and extraction testing.</p>

  <h3>Can't I just use an AI myself?</h3>
  <p>You can, and it might help with text. But AI alone cannot run the Brutal Copy-Paste Test, determine if your PDF is an image, or inspect a .DOCX for hidden tables. Our value is human verification augmented by AI efficiency.</p>

  <h2>What You'll Receive & Timing</h2>

  <h3>What's in the audit report?</h3>
  <p>A clear, actionable document containing:</p>
  <ul>
    <li><strong>Overall Assessment:</strong> High/Medium/Low ATS compatibility.</li>
    <li><strong>Confirmed Issues & Likely Risks:</strong> Directly observed failures and inferred problems.</li>
    <li><strong>Keyword Alignment:</strong> Matched and missing terms vs. your target job.</li>
    <li><strong>Weak Bullets:</strong> Specific lines with suggested rewrites.</li>
    <li><strong>Prioritized Fix List:</strong> Exact, line-by-line corrections.</li>
  </ul>
  <p>No flattery. No filler.</p>

  <h3>Do you rewrite my entire resume?</h3>
  <p>No. We provide targeted edits, rewrites for weak sections, and structural recommendations. You remain the author; we act as your technical editor and ATS mechanic.</p>

  <br>
  
  <a href="/" class="back-link">&larr; Back to StoicResume</a>

  <footer style="margin-top: 50px; padding-top: 20px; border-top: 1px solid #eaeaea; text-align: center; font-size: 13px; color: #666;">
    &copy; 2026 StoicResume
  </footer>

</body>
</html>
