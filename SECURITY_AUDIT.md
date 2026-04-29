# Security Audit
#NY Caffeine Website Prototype

# Scope

This was a beginner-friendly security review of a static front-end website prototype.  
No private systems were accessed, scanned, exploited, or tested.

# Type of Review

Public-facing website security review / basic front-end security audit.

# Findings

# 1.No Sensitive Data Collected

The website does not collect usernames, passwords, payments, addresses, or customer messages.

**Risk:** Low  
**Reason:** Since there are no forms or authentication features, there is limited risk of exposing customer data.

**Recommendation:** If forms or ordering features are added later, use HTTPS, input validation, secure backend handling, and spam protection.

# 2.No API Keys or Credentials Exposed

The project files do not include API keys, passwords, database credentials, or secret tokens.

**Risk:** Low  
**Recommendation:** Keep secrets out of GitHub. If APIs are added later, store secrets in environment variables.

# 3.External Links Open in New Tabs

External links such as Instagram and Google Maps use `target="_blank"`

**Risk:** Low to Medium  
**Recommendation:** Add `rel="noopener noreferrer"` to all external links for safer tab behavior

Ex: ```html
 <a href="https://www.instagram.com/nycaffeine1" target="_blank" rel="noopener noreferrer">