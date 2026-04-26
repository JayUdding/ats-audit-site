---
layout: default
---
 
 
 **The Mechanical Reality**

Hard to believe in 2026, but true: many Applicant Tracking Systems (ATS) do not read your resume correctly. They misread dates, scramble your skills into gibberish, and discard entire sections because of invisible formatting errors you will never know about.  

**This is not a conspiracy. Just mechanics.**

An ATS is not artificial intelligence evaluating your worth. It is a database ingestion pipeline with three stages: 

1. **Parse** (extract text into structured fields), 

2. **Store** (populate database tables), and

3. **Retrieve** (recruiter searches). 

Your goal is not to "impress" the machine--Stoics don't like flattery. Your goal is to *survive* the **Parse** stage and advance to human review with your name, experience, projects, and skills intact and correctly bucketed. 

Do not rely on ATS score checkers. They offer a false sense of security. They simulate one generic parser and give you an arbitrary percentag—85% compatible!—but the real world runs fifty different systems with fifty different failure modes. An app counts keywords; it cannot see the invisible table structure that actually destroys your application.

A well-designed diagnostic prompt can help you identify *likely* structural failures. But *diagnosis* is not the same as *judgment*. Knowing something might be wrong is not the same as knowing what to fix, what to ignore, and whether you will actually do it.

For that, you need Human-in-the-Loop (HIL) verification: forensic analysis by a technical auditor who tests your resume across multiple parsing scenarios and tells you exactly what is broken and how to repair it.

*Theory is good but practice is better. It is the test of theory, the confirmation of it.* 
-- Musonius Rufus (Teacher of Epictetus) 

**The Defense**

Because there is no universal standard—because Taleo, Workday, iCIMS, and many legacy government systems each speak a different mechanical dialect--you must optimize for the **lowest common denominator**. You must build defensively. 

This requires enforcing a **single-column linear text flow** with **zero floating objects**. No tables. No text boxes. No "visual alignment" that destroys machine readability. 

If your resume cannot survive the **Brutal Copy-Paste Test**, it will not survive an ATS. Below are the technical specifications for universal compliance. Deviate at any point and risk null fields or rejection.
 
 As Marcus Aurelius admonished: 

*Do nothing, not even the smallest thing, randomly or carelessly*.

Philosophy provides the principle; here is the practice.  

### The Stoic Resume Checklist (No Flattery—No Fluff—Understanding First)

You will learn to avoid: 
 
*   The Table Trap (invisible layout killers)
*   The Header Graveyard (lost contact info)
*   The Image-Only PDF (`Print-to-PDF` disasters)
*   The Ghost Text Box (unparseable dates)
*   The Column Bleed (scrambled skills)
 
---

### I. The Parse Stage: How Text Becomes Data

**1. The Input Methods**
Modern ATS use one of two ingestion methods:
*   **Text-layer extraction:** Reads the Unicode text stream embedded in DOCX/PDF (preferred, faster, more accurate).
*   **OCR/Computer Vision:** Rasterizes the page and performs optical character recognition (slower, error-prone, used when text layer is corrupted or for image-based PDFs).

**Your imperative:** Ensure the text layer is pristine so the ATS never falls back to OCR, which has 5-15% character error rates.

**2. The Schema Mapping**
Post-extraction, the parser attempts to map text to database fields:
*   **Contact:** Name, Phone, Email, LinkedIn, GitHub, Location
*   **Experience:** Company, Job Title, Start Date, End Date, Description
*   **Education:** Institution, Location, Degree, Field, Date
*   **Projects:** Project Names, Descriptions, Keywords
*   **Skills:** Keyword tokens, Categories 

**Critical constraint:** The parser uses **section headers** and **date patterns** to trigger field mapping. If it cannot identify where Experience ends and Education begins, it dumps everything into a "Notes" field where it becomes unsearchable.

---

### II. File Format Specifications

**DOCX (Word 2007+)**
*   **Standard:** Office Open XML (OOXML)
*   **Risk:** Legacy .DOC (Word 97-2003) uses binary formatting that modern parsers handle poorly. Always use .docx.
*   **Encoding:** Must be UTF-8. Non-Unicode characters (smart quotes from Mac TextEdit, certain Cyrillic or Arabic encoding schemes) render as � or ?

**PDF**
*   **Standard:** PDF/A-1a or PDF/A-1b (archival standard with embedded fonts and structure tags).
*   **Prohibition:** Never use "Print to PDF." This creates a PostScript rasterization. Use **File > Save As > PDF** or **Export > Create PDF/XPS**.
*   **Text Layer Verification:** Open the PDF in a viewer like Adobe Acrobat. Try to select a single word. If you cannot highlight text, it is an image and will OCR poorly.

**Prohibited Formats:** 
*   .TXT (loses all formatting and appears unprofessional)
*   .RTF (formatting inconsistencies across parsers)
*   .HTML (security stripping removes all formatting)
*   .JPG/.PNG (image resumes = instant rejection)

---

### III. Structural Architecture (The Hard Constraints)

**1. The Single Column Imperative**
*   **Rule:** One vertical text flow. No exceptions.
*   **Why:** Multi-column layouts (newspaper style, side-by-side skills lists, columns) cause parsers to read Line 1 of Column 1, then Line 1 of Column 2, creating concatenated gibberish.
*   **Table Prohibition:** Never use tables for layout. The parser reads row-by-row, not cell-by-cell. A two-column table for contact info (left: phone, right: email) often parses as: *"(555) 123-4567john@email.com"* as a single string.

**2. The Text Box Extermination**
*   **Rule:** Zero floating objects.
*   **Detection:** In Word, press Ctrl+A. If any text remains unselected or shows separate selection handles, it is a text box, shape, or grouped object.
*   **Consequence:** Text boxes parse as metadata artifacts or null values. Contact info in a header text box is often the first casualty.

**3. MS Header/Footer Prohibition**
*   **Rule:** No essential data in Word headers or footers.
*   **Consequence:** Many ATS strip headers/footers to remove "Page 1 of 2" metadata. If your name and phone number are there, they vanish.

**4. Section Header Standardization**
*   **Rule:** Use conventional strings.
*   **Compliant:** `EXPERIENCE`, `WORK EXPERIENCE`, `PROFESSIONAL EXPERIENCE`, `EMPLOYMENT`, `EDUCATION`, `PROJECTS`, `SKILLS`, `SUMMARY`, `PROFESSIONAL SUMMARY`
*   **Non-compliant or Risky:** `My Journey`, `About Me`, `Career Highlights`, `What I Bring to the Table`, `Proficiencies` (parsers may lack the NLP training to map these synonyms; they default to dumping the section into unsearchable text).

**5. Date Format Consistency**
*   **Rule:** Use unambiguous, separable formats.
*   **Compliant:** `Jan 2023 - Mar 2025`, `2023-2025`, `03/2023 - 03/2025` (though slashes can trigger date math errors in some systems). Also `Present` works...  
*   **Non-compliant Risks:**  `Current`, `Till date` or `To date` (parsers calculate tenure via date math); better to use `April 2026` or simply `Present`.  
*   **Critical:** Dates must be on the same line as or immediately adjacent to the Job Title/Company. Dates floating in right-aligned table cells often attach to the wrong record.

---

### IV. Content Encoding Hazards

**1. Special Characters & Encoding**
*   **Bullet Points:** Use standard hyphen `-` or ASCII asterisk `*`. Avoid Unicode bullets (•, ○, ●) which may render as � or be stripped entirely.
*   **Accents:** José, résumé are generally safe in UTF-8, but verify the PDF embedding (some fonts subset poorly).
*   **Symbols:** The "en dash" (–) in date ranges is safer than "em dash" (—) which can trigger line-break errors.
*   **Math Symbols:** Avoid using ≥, ≤, →, ⇒ in skills sections. Write "Proficient in Python" not "Python ⇒ Expert".

-----


**A Detailed Note on Pipes**

*     **The Pipe `|` Rule: Metadata Only, Never Content**

The pipe is a **delimiter**, not a punctuation mark. It separates distinct data fields so the parser knows where one stops and another starts. Use it in **headers and metadata lines only**. Never use it inside bullet points or skills lists.

 
**Where Pipes Work (Use Them Here)**

**Job/Education Headers:**
```
Software Engineer | Google | Mountain View, CA | Jan 2023 - April 2026
B.Sc. Computer Science | MIT | Cambridge, MA | 2019 - 2023
```
*Why:* The parser sees four distinct fields (Role, Company, Location, Date) separated by ASCII characters. It can bucket these correctly.

**Contact Info:**
```
San Francisco, CA | (415) 555-0199 | email@example.com
```
*Why:* It prevents the "concatenation blob" where the parser merges your city with your phone number into `San Francisco(415)555-0199`.

<hr> 

**Where Pipes Fail (Never Do This)**

**Inside Bullet Points:**
```
• Developed REST APIs | Python | Flask | reduced latency by 40%
• Managed team | Agile | Scrum | Jira | Confluence
```
*Why:* This looks like a table row to the parser. It may read `Developed REST APIs Python` as one skill, then `Flask reduced latency` as another, destroying your achievement. Use **commas** or **semicolons** instead.

**Skills Lists:**
```
Technical Skills: Python | JavaScript | React | Node.js | SQL
```
*Why:* The pipe suggests these are separate columns, not a list. The parser may alternate them with the next line (if two-column layout) creating `Python JavaScript` gibberish. Use **commas**:
```
Technical Skills: Python, JavaScript, React, Node.js, SQL
```
 
**The Visual Trap**

You think pipes look "cleaner" than commas in a skills list. They don't. They look like **table cells**, and tables are fatal.

**Correct:**
```
Backend: Python, Django, PostgreSQL, Redis
```

**Incorrect (Table Trap):**
```
Backend: Python | Django | PostgreSQL | Redis
```

**Bottom Line:** Pipes are for **structure** (separating Title from Company from Date). Commas are for **content** (listing tools within a bullet). Deviate and you risk null fields. 

----

**2. Font Specifications**
*   **Safe:** Arial, Calibri, Georgia, Times New Roman, Garamond, Helvetica.
*   **Risk:** Custom icon fonts (FontAwesome for email icons), barcode fonts, or decorative scripts. If the ATS lacks the font, it substitutes or omits the character.
*   **Size:** 10-12pt. Smaller text may be flagged as hidden metadata or OCR noise.

**3. Hyperlinks**
*   **Rule:** Plain text URLs only.
*   **Risk:** Hyperlinked text (blue underlined "LinkedIn" hiding `https://...`) often has the display text parsed, not the URL. Write: `linkedin.com/in/name` not "Connect with me". The same applies to your GitHub profile link.

---

### V. The Skills Section Reality

**1. Keyword Matching Mechanics**
ATS search functions use **Boolean and proximity operators**. Recruiters search: `("React.js" OR "React") AND ("Node.js" OR "Node")`.
*   **Rule:** List skills as comma-separated or line-broken plain text. Do not use tables, graphs, or "skill bars."
*   **Acronyms & Parentheses:** Legacy parsers rely on **exact string matching.** If the system searches for `Amazon Web Services` and you only wrote `AWS`, you fail the match.
    *   **The Acronym Rule:** Mirror the exact phrasing used in the target job description. If space permits, the safest defensive structure is to provide both: `Amazon Web Services (AWS)`.
    *   **The Modifier Trap:** Never use parentheses to describe your proficiency. If you write "React (expert)", dumb parsers extract the entire phrase as a single skill. When the recruiter searches for "React", your profile will return a null match.

**2. The "Keyword Stuffing" Fallacy**
Early 2000s ATS counted keyword density. Modern systems (post-2015) flag exact repetition or white-text keyword blocks as spam. Do not list "Python" 15 times in white text at the bottom. You will be rejected.

---

### VI. Visual Elements That Kill Parsing

**1. Graphics & Logos**
*   **Company Logos:** If you worked at Google, do not insert the Google logo image. The parser sees `image001.png`, not "Google."
*   **Certification Badges:** CompTIA, AWS, or LinkedIn badges are images. If the text is baked into the image, it is invisible. If you must include them, ensure the certification name appears in plain text adjacent to the badge.

**2. Lines and Separators**
*   **Horizontal Rules:** Use the Word horizontal line function (border tool), not inserted shapes or underscores. Shapes create floating anchors that disrupt text flow extraction.

**3. Color and Shading**
*   **Contrast:** Dark text on white only. Background shading (grey boxes for skills) often rasterizes the enclosed text or triggers OCR misreads.
*   **Invisible Ink:** Never use white text on white background to hide keywords. Modern PDF extractors read the text layer regardless of color; spam filters flag this as manipulation.

---

### VII. The Verification Protocol

Before submitting, perform these three tests:

**Test 1: The Brutal Copy-Paste Test**

**Windows**: Select all (Ctrl+A) → Copy → Paste into **Notepad**.

**Mac**: Command+A  (⌘+A)—Select All;  text highlights in blue; Command+C (⌘+C)—Copy (Press twice to ensure clipboard updates); Open **TextEdit (not Notepad)**; Shift+Command+T—Convert to Plain Text (removes formatting); Command+V (⌘+V)—Paste into TextEdit. 

*   **Pass:** Text flows top-to-bottom, left-to-right, chronologically. Dates follow titles. No missing sections.
*   **Fail:** Text out of order, dates floating alone, missing contact info, gibberish characters.

**Test 2: The PDF Text Extraction**
Open the final PDF. File > Save as Text (or use `pdftotext` command line).
*   **Pass:** Readable, linear output matching the Word doc.
*   **Fail:** Blank file, image warnings, scrambled text order.

**Test 3: The .docx Autopsy (If you have Word or use LibreOffice Writer's equivalent view)**
*   Enable "Show Formatting Marks" (¶). Look for table gridlines, text box borders, or section breaks.
*   Check Headers/Footers (Double-click margins) for hidden contact info.
*   Select All: Ensure everything highlights uniformly.

---

  
### VIII. The File Name Variable 

While not parsing per se, ATS ingestion often uses filename OCR for initial routing. 
*   **Compliant:** `FirstName_LastName_Computer_Engineer.pdf`
*   **Non-compliant:** `Resume_Final_v3_(1).pdf` or `My Resume.pdf` (causes overwrite conflicts and identification failures).

---

### IX. Summary Commandments

1.  **One column.** Never two. Tables are forbidden.
2.  **No floating objects.** Text boxes, shapes, and wrapped images are banned.
3.  **No headers/footers.** All data in the body.
4.  **Standard headers.** Use conventional section titles.
5.  **Save, don't print.** PDF via Export, not Print to PDF.
6.  **Test the text layer.** Copy-paste to Notepad or TextEdit: must yield perfect linear text.
7.  **Dates adjacent.** Never right-align dates via tables or tabs.
8.  **Plain text only.** Graphics are invisible; skill bars are useless.

**Violate any one of these, and you are gambling with  data integrity.**


---

   
 ---

### The Free Prompt

We offer a free diagnostic prompt you can run in any capable LLM. Upload your resume, paste the prompt, and it will likely flag ATS failures: tables, text boxes, header graveyards, column bleed, encoding errors. It works. It will catch real problems but it cannot make you act on these findings. Most people simply cannot audit their own resume objectively. AI models—*unless specifically instructed not to*—will flatter you.

  
---

### The Service

**ATS Compliance Audit —  $20**

A complete forensic audit of your resume for ATS compliance. Not a score. Not a percentage. A detailed pass/fail report listing every parsing failure, every structural risk, and the exact fix for each.

**What you receive:**

- **Structural analysis**: tables, text boxes, floating objects, header/footer content, column detection.
- **Encoding audit**: character rendering, bullet consistency, date format compliance, font safety.
- **Section mapping review**: whether your headers trigger correct field mapping or dump into unsearchable text.
- **The Brutal Copy-Paste Test**: performed manually, with annotation of every failure point.
- **Specific Corrections**: not "consider revising"—exact changes, line by line.

**Included: Keyword Alignment Analysis**

You may submit one target job posting *along* with your resume. We extract the likely recruiter search queries and show you how to align your resume to match—correct placement, correct phrasing, correct field mapping so the terms land where the Boolean search will find them.

---

### How It Works

1. **Pay:** via Stripe or Bitcoin using the buttons below.
2. **Submit:**  your resume (PDF or Word) and one target job posting to audit@stoicresume.com. If paying via Bitcoin, include your transaction ID.
3. **Receive:** Within 24 hours, your full HIL diagnostic report. No flattery. No filler. Just findings and fixes.

---

### The Guarantee

**7-Day Refund.** If the audit does not meet your expectations, email within 7 days. Full refund. No questions.

**Privacy.** Your resume and email are permanently deleted 7 days after delivery. We do not retain, sell, or share your data.

---

### The Choice

Use the free prompt if you trust yourself to judge your own work without bias.

Use the audit if you want the truth from someone who has no attachment to your formatting.


As Epictetus observed: *"It is impossible for a man to learn what he thinks he already knows."*





---


<style>
  .testimonials-section {
    margin-top: 3rem;
    padding-top: 2rem;
    border-top: 1px solid #2E7D8C;
  }
  .testimonials-scroll {
    display: flex;
    gap: 1.5rem;
    overflow-x: auto;
    padding-bottom: 1.5rem;
    scroll-snap-type: x mandatory;
    -webkit-overflow-scrolling: touch;
  }
  .testimonial-card {
    flex: 0 0 300px;
    scroll-snap-align: start;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background: #ffffff;
    padding: 1.5rem;
    border-radius: 8px;
    border: 1px solid #eff0f1;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
  }
  .testimonial-text {
    margin: 0 0 1rem 0;
    font-style: italic;
    color: #2E7D8C;
    font-size: 0.95rem;
    line-height: 1.5;
  }
  .testimonial-author {
    display: block;
    font-weight: bold;
    font-style: normal;
    color: #2E7D8C;
    font-size: 0.9rem;
  }
  .testimonials-scroll::-webkit-scrollbar {
    height: 8px;
  }
  .testimonials-scroll::-webkit-scrollbar-track {
    background: #f1f1f1;
    border-radius: 4px;
  }
  .testimonials-scroll::-webkit-scrollbar-thumb {
    background: #d1d5da;
    border-radius: 4px;
  }
  .testimonials-scroll::-webkit-scrollbar-thumb:hover {
    background: #a3a8ae;
  }
  @media (max-width: 500px) {
    .testimonial-card {
      flex: 0 0 85%;
    }
  }
</style>

<div class="testimonials-section">
  <h3>What People Are Saying</h3>
  <div class="testimonials-scroll">

    <!-- Testimonial 1 -->
    <div class="testimonial-card">
      <p class="testimonial-text">
        "Solid review. Glad I got my resume correct."
      </p>
      <span class="testimonial-author">— ML, Graduate Student</span>
    </div>

    <!-- Testimonial 2 -->
    <div class="testimonial-card">
      <p class="testimonial-text">
        "Thanks for the 'brutal' truth but I can handle it. Fixed a key error."
      </p>
      <span class="testimonial-author">— DM, Student</span>
    </div>

    <!-- Testimonial 3 -->
    <div class="testimonial-card">
      <p class="testimonial-text">
        "5 stars for you! Very useful."
      </p>
      <span class="testimonial-author">— KF, Engineer</span>
    </div>

    <!-- Testimonial 4 -->
    <div class="testimonial-card">
      <p class="testimonial-text">
        "This document is incredibly useful. In fact it is absolute gold."
      </p>
      <span class="testimonial-author">— Claude</span>
    </div>

   

  
</div>

<!-- === MAIN CALL-TO-ACTION SECTION === -->
<div class="action-buttons-wrapper">

  <!-- 0. The Stripe/Fiat Button (Primary Purchase) -->
  <a href="YOUR_STRIPE_LINK_HERE" class="stripe-promo-btn">
    <div class="btn-main-text" style="color: white; text-decoration: none;">
      <svg width="22" height="22" fill="currentColor" viewBox="0 0 24 24" style="vertical-align: middle; margin-right: 8px; margin-bottom: 3px;"><path d="M20 4H4c-1.11 0-1.99.89-1.99 2L2 18c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V6c0-1.11-.89-2-2-2zm0 14H4v-6h16v6zm0-10H4V6h16v2z"/></svg>
      Order Full Audit — $20
    </div>
    <div class="btn-sub-text" style="color: #e0e0e0;">Secure checkout via Stripe</div>
  </a>

  <!-- 1. The Bitcoin Button (Discount Purchase) -->
  <a href="bitcoin:bc1qnrrvx2qp04mpq0jqmq0r59wwyn2qyw79c7plfl6akmxe3c4dnq5sjhjhm2?message=AuditATS" class="btc-promo-btn" id="btc-button" onclick="handleBitcoinClick(event)">
    <div class="btn-main-text">
      <img src="https://upload.wikimedia.org/wikipedia/commons/4/46/Bitcoin.svg" alt="Bitcoin Logo" width="24" height="24" style="vertical-align: middle; margin-right: 8px; margin-bottom: 3px;">
      Order Full Audit — <s>\$20</s> <strong>\$10</strong>
    </div>
    <div class="btn-sub-text">Pay with Bitcoin & Save 50%</div>
  </a>

  <!-- 2. The Free Download Button (Secondary) -->
  <a href="./free-prompt.html" target="_blank" rel="noopener noreferrer" class="free-prompt-btn">
    <div class="btn-main-text" style="color: inherit;">
      <svg width="20" height="20" fill="currentColor" viewBox="0 0 24 24" style="vertical-align: middle; margin-right: 8px; margin-bottom: 3px;"><path d="M19 9h-4V3H9v6H5l7 7 7-7zM5 18v2h14v-2H5z"/></svg>
      Get the Free Prompt
    </div>
    <div class="free-btn-sub">Test your own resume in ChatGPT</div>
  </a>
  

</div>

<!-- === THE BITCOIN FALLBACK MODAL === -->
<div id="btc-modal" class="btc-modal">
  <div class="btc-modal-content">
    <span class="btc-modal-close" onclick="closeModal()">&times;</span>
    <h2 style="margin-top: 0;">Pay with Bitcoin</h2>
    <p>Please Send <strong>  $10 USD worth of Bitcoin</strong> to this address:</p>
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=bitcoin:bc1qnrrvx2qp04mpq0jqmq0r59wwyn2qyw79c7plfl6akmxe3c4dnq5sjhjhm2" alt="Bitcoin QR Code" style="margin: 15px 0;">
    <div class="btc-address-box">
      <code id="btc-address">bc1qnrrvx2qp04mpq0jqmq0r59wwyn2qyw79c7plfl6akmxe3c4dnq5sjhjhm2</code>
      <button onclick="copyAddress()" class="copy-btn">Copy</button>
    </div>
    <p style="font-size: 13px; color: #666; margin-top: 15px;">
      After sending, email your resume + transaction ID to:<br>
      <strong>audit@stoicresume.com</strong>
    </p>
  </div>
</div>

<!-- === ALL CSS STYLES === -->
<style>
  /* --- Layout Wrapper (Controls the side-by-side and spacing) --- */
  .action-buttons-wrapper {
    display: flex;
    flex-direction: row;         
    flex-wrap: wrap;             
    justify-content: center;     
    align-items: stretch;        
    gap: 25px;                   
    margin-top: 50px;            
    margin-bottom: 60px;         
    padding: 0 20px;
    font-family: Arial, sans-serif;
  }

  /* --- General Button Styles --- */
  .stripe-promo-btn, .btc-promo-btn, .free-prompt-btn {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    padding: 16px 24px;
    border-radius: 8px;
    transition: all 0.2s ease;
    width: 320px;                
    box-sizing: border-box;
    text-align: center;
  }

  /* --- Stripe Button Specifics --- */
  .stripe-promo-btn {
    background-color: #2c6c75;
    color: white;
    border: 2px solid #2c6c75;
    box-shadow: 0 4px 10px rgba(44, 108, 117, 0.2);
  }
  .stripe-promo-btn:hover {
    background-color: #1f4f56;
    border-color: #1f4f56;
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(44, 108, 117, 0.3);
  }

  /* --- Bitcoin Button Specifics --- */
  .btc-promo-btn {
    background-color: #F7931A;
    color: white;
    border: 2px solid #F7931A;
    box-shadow: 0 4px 10px rgba(247, 147, 26, 0.2);
  }
  .btc-promo-btn:hover {
    background-color: #e08316;
    border-color: #e08316;
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(247, 147, 26, 0.3);
  }
  .btn-sub-text {
    font-size: 14px;
    font-weight: normal;
    opacity: 0.9;
    margin-top: 6px;
  }

  /* --- Free Prompt Button Specifics --- */
  .free-prompt-btn {
    background-color: transparent;
    color: #347b85;
    border: 2px solid #347b85;
  }
  .free-btn-sub {
    font-size: 14px; 
    margin-top: 6px; 
    color: #666;
    transition: color 0.2s ease;
  }
  .free-prompt-btn:hover {
    background-color: #347b85;
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(52, 123, 133, 0.2);
  }
  .free-prompt-btn:hover .free-btn-sub {
    color: white; 
  }

  /* Shared Text Style */
  .btn-main-text {
    font-size: 18px;
    font-weight: bold;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  /* --- Modal Styles (Unchanged) --- */
  .btc-modal { display: none; position: fixed; z-index: 1000; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.6); }
  .btc-modal-content { background-color: #fff; padding: 30px; border-radius: 12px; text-align: center; max-width: 400px; margin: 10% auto; box-shadow: 0 5px 30px rgba(0,0,0,0.3); color: #333; }
  .btc-modal-close { float: right; font-size: 28px; font-weight: bold; color: #aaa; cursor: pointer; line-height: 1; }
  .btc-modal-close:hover { color: #333; }
  .btc-address-box { background-color: #f4f4f4; padding: 12px; border-radius: 6px; display: flex; justify-content: space-between; align-items: center; gap: 10px; margin-top: 10px; }
  .btc-address-box code { font-size: 11px; word-break: break-all; color: #333; }
  .copy-btn { background-color: #F7931A; color: white; border: none; padding: 8px 14px; border-radius: 5px; cursor: pointer; font-weight: bold; }
  .copy-btn:hover { background-color: #e08316; }

  /* --- Mobile Responsiveness --- */
  @media (max-width: 700px) {
    .action-buttons-wrapper {
      flex-direction: column;      
      align-items: center;
      gap: 15px;
    }
    .stripe-promo-btn, .btc-promo-btn, .free-prompt-btn {
      width: 100%;                 
      max-width: 320px;
    }
  }
</style>

<!-- === JAVASCRIPT === -->
<!-- (Keep your exact Javascript here, no changes needed) -->
<script>
  function handleBitcoinClick(event) {
    var start = Date.now();
    setTimeout(function() {
      if (Date.now() - start < 1500) {
        document.getElementById('btc-modal').style.display = 'block';
      }
    }, 1000);
  }
  function closeModal() { document.getElementById('btc-modal').style.display = 'none'; }
  function copyAddress() {
    var address = document.getElementById('btc-address').innerText;
    navigator.clipboard.writeText(address);
    alert('Bitcoin address copied to clipboard!');
  }
  window.onclick = function(event) {
    var modal = document.getElementById('btc-modal');
    if (event.target == modal) { modal.style.display = 'none'; }
  }
</script>

<!-- START: GLOBAL FOOTER (Place this at the very bottom of your body tag) -->
<footer style="margin-top: 50px; padding-top: 20px; border-top: 1px solid #eaeaea; text-align: center; font-size: 13px; color: #666;">
  <p>
    Questions or success stories? Email us at <a href="mailto:info@stoicresume.com" style="color: #2c6c75;">info@stoicresume.com</a>
  </p>
  <p>
    &copy; 2026 StoicResume.com | 
    <a href="privacy.html" style="color: #666; text-decoration: underline;">Privacy Policy & Terms</a> | 
    7-Day Refund Guarantee
  </p>
</footer>
<!-- END: GLOBAL FOOTER -->

