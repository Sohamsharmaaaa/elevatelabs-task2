# Phishing Email Analysis Report

## Task Overview
**Objective**: Analyze a suspicious email sample to identify phishing characteristics and threats  
**Date**: 3 July 2025  
**Analyst**: Soham Sharma
**Tools Used**: MXToolbox Email Header Analyzer, EML Analyzer

---

## Email Sample Details

**Subject**: CLIENTE PRIME - BRADESCO LIVELO: Seu cartão tem 92.990 pontos LIVELO expirando hoje!  
**From**: BANCO DO BRADESCO LIVELO <banco.bradesco@atendimento.com.br>  
**To**: phishing@pot  
**Date**: Wed 2023-09-20 00:05  
**Message ID**: <20230919183549.39DEA3F725@ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06>

---

## Phishing Indicators Identified

### 1. **Sender Email Address Analysis**
- **Suspicious Domain**: `atendimento.com.br` instead of legitimate `bradesco.com.br`
- **Domain Spoofing**: Attackers registered a similar-looking domain to impersonate Bradesco
- **Legitimacy Check**: Real Bradesco emails would come from `@bradesco.com.br` or verified subdomains

### 2. **Email Header Analysis Results**

#### Authentication Failures:
- **DMARC**: ❌ Not Compliant (No DMARC Record Found)
- **SPF**: ❌ Not Authenticated 
- **DKIM**: ❌ Not Authenticated
- **Authentication Result**: `spf=temperror`, `dkim=none`, `dmarc=temperror`

#### Technical Red Flags:
- **Sender IP**: 137.184.34.4 (Suspicious origin)
- **Server**: Ubuntu server (unusual for legitimate banking emails)
- **Delivery Path**: Shows signs of email spoofing through multiple hops

#### Social Engineering Elements:
- **False Scarcity**: Claims points expire "today"
- **Value Proposition**: Mentions "92.990 MIL PONTOS" (92,990 points)
- **Legitimate Branding**: Uses Bradesco and Livelo branding to appear authentic
- **Multiple CTAs**: Various redemption options (miles, discounts, catalog items)

### 4. **Language and Grammar Issues**
- **Inconsistent Capitalization**: "Você Clientes Banco do Bradesco"
- **Grammar Errors**: "Descontos de ate 35%" (missing accent: "até")
- **Spelling Issues**: "aereas" instead of "aéreas"
- **Poor Formatting**: Inconsistent spacing and punctuation

### 5. **Suspicious Links and Attachments**
- **Call-to-Action Buttons**: "Resgatar Agora" button likely leads to phishing site
- **No Legitimate Contact Info**: Missing official Bradesco contact details
- **Redirect Risk**: Links would likely redirect to credential harvesting pages

---

## Risk Assessment

### **Risk Level: HIGH**

### Potential Threats:
1. **Credential Theft**: Users clicking links may be redirected to fake login pages
2. **Identity Theft**: Personal and financial information harvesting
3. **Financial Fraud**: Unauthorized access to banking accounts
4. **Malware Distribution**: Potential for malicious downloads
5. **Account Takeover**: Compromised banking credentials

![Screenshot 2025-07-03 104136](https://github.com/user-attachments/assets/bb953246-b8d3-4976-b7bc-4c12c7394930)

![Screenshot 2025-07-03 104211](https://github.com/user-attachments/assets/5a834a6d-15c7-4f41-bbc0-7ae1374abd2e)

![Screenshot 2025-07-03 103926](https://github.com/user-attachments/assets/6d856969-a1ea-40fd-baf9-c82a51ad6912)

![Screenshot 2025-07-03 103950](https://github.com/user-attachments/assets/b5d15bbe-983a-429f-82de-49350a220bd6)

