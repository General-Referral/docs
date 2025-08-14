# General Referral Knowledge Base Editor Playbook

*A step-by-step guide for non-technical users to add and update knowledge base articles*

## Table of Contents
1. [Getting Started](#getting-started)
2. [Understanding the Knowledge Base Structure](#understanding-the-knowledge-base-structure)
3. [Adding New Articles](#adding-new-articles)
4. [Editing Existing Articles](#editing-existing-articles)
5. [Using Mintlify Components](#using-mintlify-components)
6. [Content Guidelines](#content-guidelines)
7. [Publishing Changes](#publishing-changes)
8. [Troubleshooting](#troubleshooting)
9. [Quick Reference](#quick-reference)

---

## Getting Started

### What You Need
- Access to your Mintlify account (contact admin for invite)
- A web browser (Chrome, Firefox, Safari, or Edge)
- Basic writing skills (no coding required!)

### How Mintlify Works
Mintlify provides a **web-based editor** that allows you to edit articles directly in your browser with two modes:
- **Visual Mode**: WYSIWYG editor like Microsoft Word - what you see is what gets published
- **Markdown Mode**: For users comfortable with simple text formatting

No technical setup required - everything happens in your browser!

---

## Understanding the Knowledge Base Structure

### Current Sections
Your knowledge base has 4 main sections:

```
📁 Getting Started
   ├── How to Sign Up
   ├── Cost to Hang Your License
   ├── NJ Restrictions
   └── [other articles...]

📁 Referral Transactions
   ├── How to Submit a Referral
   ├── How to Get Paid
   └── [other articles...]

📁 Membership Management
   ├── State License Renewal
   ├── Update Payment Method
   └── [other articles...]

📁 Sales Training
   ├── Finding Leads
   ├── Prospecting Scripts
   └── [other articles...]
```

### File Naming Rules
- Article files end with `.mdx`
- Use lowercase letters and dashes (no spaces)
- Examples: `how-to-sign-up.mdx`, `nj-restrictions.mdx`

---

## Adding New Articles

### Step 1: Access Mintlify Web Editor
1. Go to your Mintlify documentation site
2. Log in with your Mintlify account credentials
3. Navigate to the web editor (usually an "Edit" button or editor link)
4. Choose the appropriate section folder (getting-started, referral-transactions, etc.)

### Step 2: Create a New File
1. Click the **"New File"** or **"Create"** button in the web editor
2. Name your file following the pattern: `your-article-title.mdx`
3. Choose the appropriate folder/section for your article

### Step 3: Add the Article Header
Every article must start with this header (called "frontmatter"):

```yaml
---
title: Your Article Title Here
description: A brief description of what this article covers
---
```

**Example:**
```yaml
---
title: How to Update Your Phone Number
description: Step-by-step guide to changing your contact information in the member portal
---
```

### Step 4: Choose Your Editing Mode

**Visual Mode (Recommended for beginners):**
- Point-and-click editing like Microsoft Word
- Insert components using the component menu
- See exactly how your article will look
- No need to learn Markdown syntax

**Markdown Mode (For advanced users):**
- Direct text editing with formatting codes
- Full control over article structure
- Use when you need precise formatting

### Step 5: Write Your Content
- Use the visual editor's toolbar for formatting
- Insert Mintlify components from the component menu
- Preview your changes in real-time
- Save your work frequently

### Step 6: Navigation Updates
**Automatic:** Mintlify's web editor can automatically update the navigation menu when you create new articles, depending on your setup.

---

## Editing Existing Articles

### Method 1: Mintlify Web Editor (Recommended)
1. Go to your Mintlify documentation site
2. Navigate to the article you want to edit
3. Click the **"Edit"** button (available with your Mintlify plan)
4. Choose Visual Mode or Markdown Mode
5. Make your changes and save

### Method 2: GitHub (Backup Method)
1. Navigate to the article file in GitHub
2. Click the **pencil icon (✏️)** to edit
3. Make your changes in Markdown
4. Scroll down and click **"Commit changes"**

<Info>
The web editor is much easier for non-technical users and provides real-time preview of your changes.
</Info>

---

## Using Mintlify Components

### Visual Mode (Recommended)
In the web editor's Visual Mode, use the **Component Menu** to easily insert:
- Info boxes, warnings, and tips
- Step-by-step instructions
- Expandable sections (accordions)
- Navigation cards
- Tabbed content
- Video frames

### Markdown Mode
If using Markdown Mode or GitHub, here are the component codes:

### Info Boxes

**For important information:**
```markdown
<Info>
Your important message here
</Info>
```

**For tips:**
```markdown
<Tip>
Your helpful tip here
</Tip>
```

**For warnings:**
```markdown
<Warning>
Important warning message here
</Warning>
```

### Step-by-Step Instructions
```markdown
<Steps>
  <Step title="First Step">
    Explain what to do first
  </Step>
  <Step title="Second Step">
    Explain the next step
  </Step>
  <Step title="Final Step">
    Explain the last step
  </Step>
</Steps>
```

### Expandable Sections (Accordions)
```markdown
<AccordionGroup>
  <Accordion title="Frequently Asked Question 1">
    Your answer goes here
  </Accordion>
  <Accordion title="Frequently Asked Question 2">
    Another answer goes here
  </Accordion>
</AccordionGroup>
```

### Navigation Cards
```markdown
<CardGroup cols={2}>
  <Card title="Related Article 1" icon="user" href="/knowledge-base/section/article-name">
    Brief description of what this link contains
  </Card>
  <Card title="Related Article 2" icon="dollar-sign" href="/knowledge-base/section/other-article">
    Brief description of this other link
  </Card>
</CardGroup>
```

### Tabbed Content
```markdown
<Tabs>
  <Tab title="Option A">
    Content for the first tab
  </Tab>
  <Tab title="Option B">
    Content for the second tab
  </Tab>
</Tabs>
```

### YouTube Videos
```markdown
<Frame>
  <iframe 
    width="100%" 
    height="400" 
    src="https://www.youtube.com/embed/VIDEO_ID_HERE" 
    frameborder="0" 
    allowfullscreen
  />
</Frame>
```

---

## Content Guidelines

### Writing Style
- **Use "you"** - Write directly to the reader ("You should click here")
- **Be conversational** - Write like you're talking to a friend
- **Keep it simple** - Use everyday language, not jargon
- **Be specific** - Give exact steps and examples

### Structure Your Articles
1. **Start with a brief overview** of what the article covers
2. **Use headings** to break up long sections
3. **Include examples** whenever possible
4. **End with next steps** or related articles

### Essential Elements
- **Title**: Clear and descriptive
- **Description**: 1-2 sentence summary
- **Headings**: Use ## for main sections, ### for subsections
- **Links**: Always test that your links work

### What to Include
✅ **Do include:**
- Step-by-step instructions
- Screenshots when helpful
- Contact information for support
- Links to related articles
- FAQs for complex topics

❌ **Don't include:**
- Broken links
- Outdated information
- Internal company jargon
- Assumptions about user knowledge

---

## Publishing Changes

### Web Editor Publishing
**Option 1: Direct Publishing**
- Click **"Publish"** to immediately update your live knowledge base
- Changes appear within 1-2 minutes

**Option 2: Pull Request (for review)**
- Click **"Create Pull Request"** to submit changes for review
- Someone with approval rights can review and publish
- Ideal for collaborative editing

### GitHub Publishing
- Changes made in GitHub automatically publish to your live site
- May take 2-5 minutes to appear

### How to Check Your Changes
1. Wait 1-3 minutes after publishing
2. Visit your knowledge base website
3. Navigate to the article you changed
4. Verify your changes appear correctly

---

## Troubleshooting

### Common Issues and Solutions

**Problem:** "I can't access the web editor"
**Solution:** Contact your Mintlify admin to ensure you have editor permissions. The web editor requires a Mintlify account with editing rights.

**Problem:** "My article isn't showing in the navigation menu"
**Solution:** The web editor should automatically handle navigation updates. If not, contact your admin or check the navigation settings.

**Problem:** "My formatting looks wrong in Visual Mode"
**Solution:** Switch between Visual and Markdown modes to troubleshoot. The Visual Mode shows exactly how it will appear when published.

**Problem:** "My links don't work"
**Solution:** 
- For internal links: Use the full path like `/knowledge-base/section/article-name`
- For external links: Include `https://` at the beginning

**Problem:** "I can't find the edit button on my live site"
**Solution:** The edit button availability depends on your Mintlify plan and permissions. Contact your admin if you should have access but don't see it.

**Problem:** "My YouTube video won't display"
**Solution:** Make sure you're using the `embed` version of the YouTube URL, not the regular watch URL.

### Getting Help
- **For content questions:** Contact the team member responsible for knowledge base content
- **For technical issues:** Contact your development team or Mintlify support
- **For urgent fixes:** Make a note of the issue and contact both content and technical teams

---

## Quick Reference

### Article Template
```markdown
---
title: Your Article Title
description: Brief description of the article
---

## Introduction

Brief overview of what this article covers.

## Step-by-Step Instructions

<Steps>
  <Step title="First Step">
    What to do first
  </Step>
  <Step title="Second Step">
    What to do next
  </Step>
</Steps>

## Important Notes

<Info>
Any important information users should know
</Info>

## Frequently Asked Questions

<AccordionGroup>
  <Accordion title="Common Question">
    Your answer here
  </Accordion>
</AccordionGroup>

## Next Steps

<CardGroup cols={2}>
  <Card title="Related Article" href="/knowledge-base/section/article">
    Link to related content
  </Card>
</CardGroup>
```

### Common Links You'll Need
- Member Portal: `https://app.generalreferral.com/members`
- Plans Page: `https://www.generalreferral.com/plans`
- Contact Form: `https://app.generalreferral.com/contact`
- Commission Calculator: `https://www.generalreferral.com/commission-calculator`

### File Naming Examples
- `how-to-sign-up.mdx` ✅
- `cost-to-hang-license.mdx` ✅  
- `How To Sign Up.mdx` ❌ (no caps, no spaces)
- `how_to_sign_up.mdx` ❌ (use dashes, not underscores)

### Section Folders
- `getting-started/` - Onboarding and basic info
- `referral-transactions/` - Making and managing referrals  
- `membership-management/` - Account and license management
- `sales-training/` - Business growth and marketing

---

## Final Tips

1. **Start small** - Edit an existing article first to get comfortable
2. **Preview your changes** - Always check how your article looks after publishing
3. **Keep it updated** - Review articles regularly and update outdated information
4. **Ask for help** - Don't hesitate to reach out when you need assistance
5. **Save often** - Make sure to save/commit your changes frequently

Remember: You're helping real estate agents succeed in their referral business. Clear, helpful content makes a real difference in their success!

---

*Last updated: [Current Date]*
*For technical questions about this playbook, contact: [Technical Team Contact]*