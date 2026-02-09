---
layout: page
title: Whoami
permalink: /about/
---
<style>
  .terminal-container {
    background: #0c0c0c;
    border: 2px solid #1a1a1a;
    border-radius: 8px;
    padding: 20px;
    margin: 2rem auto;
    max-width: 900px;
    font-family: 'Consolas', 'Courier New', monospace;
    box-shadow: 0 0 20px rgba(0, 255, 0, 0.1);
    position: relative;
  }

  .terminal-header {
    background: #1a1a1a;
    margin: -20px -20px 20px -20px;
    padding: 8px 15px;
    border-bottom: 1px solid #333;
    font-size: 13px;
    color: #888;
  }

  .terminal-title {
    display: inline-block;
  }

  .terminal-buttons {
    float: right;
  }

  .terminal-buttons span {
    display: inline-block;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    margin-left: 8px;
  }

  .btn-close { background: #ff5f56; }
  .btn-minimize { background: #ffbd2e; }
  .btn-maximize { background: #27c93f; }

  .terminal-output {
    color: #c19a6b;
    font-size: 14px;
    line-height: 1.6;
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  .cmd-prompt {
    color: #c19a6b;
    margin-bottom: 10px;
  }

  .cmd-prompt::before {
    content: "C:\\Users\\Visitor>";
    margin-right: 5px;
  }

  .blink {
    animation: blink 1s infinite;
  }

  @keyframes blink {
    0%, 50% { opacity: 1; }
    51%, 100% { opacity: 0; }
  }

  .section-header {
    color: #c19a6b;
    margin-top: 20px;
    margin-bottom: 10px;
  }

  @media (max-width: 700px) {
    .terminal-container {
      padding: 15px;
      margin: 1rem;
    }

    .terminal-output {
      font-size: 12px;
    }
  }
</style>

<div class="terminal-container">
  <div class="terminal-header">
    <span class="terminal-title">cmd.exe</span>
    <div class="terminal-buttons">
      <span class="btn-minimize"></span>
      <span class="btn-maximize"></span>
      <span class="btn-close"></span>
    </div>
  </div>
  
  <div class="terminal-output">
<span class="cmd-prompt">whoami /all</span>

   User Name     . . . . . . . . . : Sameem Ahmadzai
   Role          . . . . . . . . . : Secure Infrastructure Consultant 
   Country/Region. . . . . . . . . : Sweden


   Work Experience  . . . . . . . : Detection Engineering | Threat Hunting | 
                                    Vulnerability Management | Cyber Threat 
                                    Intelligence | Security Assessments | 
                                    Basic Endpoint Forensics| Defender XDR|
                                    Entra ID | Intune


   Microsoft Certified  . . . . . : Microsoft Security Operations Analyst (SC-200)
                                    Microsoft Identity and Access Administrator 
                                    Associate (SC-300)
                                    Microsoft Azure Fundamentals (AZ-900)

<span class="cmd-prompt"><span class="blink">_</span></span>
  </div>
</div>