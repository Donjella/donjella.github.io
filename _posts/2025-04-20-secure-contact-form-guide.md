---
layout: post
title: "Create a Secure Contact Form Without Plugins: A Modern, Easy Guide"
date: 2025-04-20
---

# Build a Secure Contact Form Without Plugins: A Comprehensive Yet Easy Guide

## 1. Current and Emerging Industry Trends in Form Security

### The Evolving Threat of AI-Generated Spam

Bots are becoming increasingly sophisticated, and securing contact forms now requires more than just basic validation. AI-generated spam enables even non-technical attackers to craft personalised, convincing messages that bypass traditional filters and target vulnerable form endpoints. Tools like WormGPT and FraudGPT allow phishing content to be generated at scale (Law, 2025), making simple defences such as basic validation or standalone CAPTCHAs less effective.

AI is fundamentally transforming the cyberfraud landscape by enabling attackers to scale operations, refine tactics, and bypass security measures with unprecedented efficiency. AI-powered botnets can dynamically adapt their behaviour, make autonomous decisions, and respond in real time to changing defences to bypass bot detection systems, making them a formidable threat to traditional security systems (Falokun, 2025).

According to recent spam statistics reports, there is a sharp rise in AI-driven spam activities. Zscaler reported a 60 percent year-over-year increase in phishing activity, while SlashNext recorded a 1,265 percent spike in malicious email volume following the release of generative AI tools. With 61 percent of phishing emails now created using AI, contact forms are becoming prime targets (Law, 2025). In 2023, over 160 billion spam emails were sent each day, accounting for 46 percent of global email traffic (Ellis & Brandl, 2024).

Australia now ranks ninth globally for phishing targets, with a 479.3 percent increase in phishing content hosted within the country. Scamwatch received 109,000 phishing reports in 2023 alone, resulting in AU$26.1 million in losses. Despite the scale of the threat, only 10 percent of Australians report being concerned or aware of AI-powered scams (Law, 2025).

### Emerging Security Approaches

The security industry is responding with more sophisticated defence mechanisms:

- **Behavioural Analysis**: Beyond simple honeypots, modern security solutions analyse typing patterns, mouse movements, and interaction behaviours to differentiate humans from bots.
- **Time-Based Defence Strategies**: More sophisticated than basic time checks, these systems establish baselines of expected completion times and flag submissions that deviate significantly.
- **Multi-layered Validation**: The industry is moving toward comprehensive protection that combines client-side convenience with robust server-side security.
- **Privacy-Focused Validation**: With the rise of privacy regulations like GDPR and Australia's Privacy Act, there's a growing trend toward implementing security measures that don't compromise user privacy.

The most effective form protection combines multiple verification layers while maintaining a seamless user experience (Umapathy, 2024).

### Opportunities

The increasing prevalence of AI-generated spam presents an important opportunity for developers to build and apply real-world security solutions. This project demonstrates how even junior developers can address a modern, evolving threat by applying industry-relevant tools in a practical context.

By securing a common and often overlooked feature like a contact form, developers not only protect users but also gain valuable experience with ethical coding practices and proactive cybersecurity strategies. Moreover, the current landscape of resources is limited—when searching for 'secure contact form tutorials' on Google or YouTube, most results direct users to WordPress plugins such as 'Contact Form 7' and 'Fast Secure Form', or third-party form handlers like FormSubmit.co or hosting platforms such as Netlify that provide their own built-in form functionality. This gap highlights the need for educational resources on building secure contact forms from scratch with custom security implementations.

## 2. Ethical Considerations in Form Security

### Data Privacy and Minimisation

When implementing form security, developers must balance protection with privacy. The Office of the Australian Information Commissioner (OAIC) emphasises that organisations should only collect information that is reasonably necessary and take reasonable steps to protect the information from misuse, interference, and loss (Office of the Australian Information Commissioner [OAIC], 2019).

This raises several ethical considerations:

1. **Data Collection**: Every piece of information collected for security purposes (IP addresses, timestamps, browser fingerprints) represents potential privacy exposure.
2. **Transparency**: Users should understand what information is being collected and how it's being used.
3. **Proportionality**: Security measures should be proportional to the actual risk, avoiding excessive data collection.

We should implement the minimum-security measures necessary to achieve their security goals, rather than collecting maximum data.

### Emerging AI-Related Ethical Challenges

The rise of AI-generated spam has introduced new ethical complexities:

1. **Escalating Privacy Intrusions**: As bots become more sophisticated, there's pressure to implement more invasive monitoring techniques. Security measures may need to analyse typing patterns, mouse movements, and other behavioural data to distinguish humans from AI. This creates an ethical dilemma where better security might require greater privacy compromises.

2. **Algorithmic Bias in Protection Systems**: Recent studies indicate that automated security systems may disproportionately flag submissions from certain demographics. A 2023 Stanford study found that non-native English speakers were 35% more likely to be incorrectly identified as bots by common security systems (Stanford Institute for Human-Centered AI, 2023). This raises concerns about equal access to digital services.

3. **Disclosure Requirements**: The increasing use of behavioural analysis for bot detection raises questions about transparency obligations. Users have a right to know when their interactions are being analysed, but providing too much information about security measures can help attackers circumvent them.

4. **Regulatory Uncertainty**: Australia's Privacy Act review is ongoing, with proposed amendments specifically addressing AI technologies and automated decision-making. Organisations implementing security measures today must consider how these may need to adapt to emerging regulations.

### Accessibility Impact

Security measures must not create barriers for users with disabilities. The Web Accessibility Initiative notes that many security implementations create significant accessibility obstacles (W3C Web Accessibility Initiative, n.d.).

Common ethical issues include:

1. **CAPTCHA Barriers**: Traditional CAPTCHAs can be impossible for users with visual impairments.
2. **Timing Challenges**: Time-based security can disadvantage users who require more time to complete forms.
3. **Complex Interaction Requirements**: Some security measures require interactions that aren't accessible to all users.

Therefore, it is essential to adopt a security approach that remains accessible to all users while ensuring strong protection and avoiding discriminatory barriers.

### Balance Between User Experience and Security

Finding the right balance between security and usability presents an ethical challenge. Security barriers like CAPTCHAs or unnecessary data requests can reduce form completion rates. While security is important, overly complex or intrusive security measures can frustrate users and lead them to abandon the form. However, insufficient security exposes users to risks and organisations to potential data breaches (Formsort, 2023).

This project attempts to navigate this ethical tension by implementing security measures that provide robust protection while minimising user friction. The approach favours invisible security measures (server-side validation, honeypots, and reasonable time-based checks) over intrusive methods that interrupt the user experience.

By carefully balancing these ethical considerations, we aim to create a form that respects user privacy and accessibility while providing effective protection against increasingly sophisticated spam bots.

## 3. The Problem: Form Spam and Security Vulnerabilities

Contact forms are commonly targeted by bots to send spam, launch denial-of-service attacks, or exploit unvalidated inputs. This can damage a website's reputation, disrupt services, and compromise user trust.

### The Rise of Automated Attacks

Automated bots can submit forms thousands of times per hour, leading to:

- Inbox flooding with spam messages
- Increased server resource consumption
- Potential denial-of-service (DoS) attacks
- Cluttered databases filled with fake submissions

To put this into perspective, approximately 320 billion spam emails are sent daily, and 94% of malware is delivered via this medium (Winder, 2020). This underscores the scale of spam-related challenges faced by organizations and developers.

### Cross-Site Scripting (XSS) Vulnerabilities

Unsanitised form inputs can lead to cross-site scripting attacks where malicious code is injected into the application. These attacks can:

- Steal user cookies and session data
- Redirect users to malicious sites
- Deface websites
- Access sensitive data

Cross-site scripting (XSS) vulnerabilities continue to rank among the most prevalent web application security threats. According to Veracode's State of Software Security 2024 Report, XSS is consistently one of the top three most frequently identified vulnerabilities in both proprietary and open-source applications (Veracode, 2024). Hence, XSS remains a significant and ongoing concern in the field of web application security.

### Data Validation Failures

Without proper validation, forms can receive:

- Malformed data that breaks application functionality
- Excessively large inputs that consume server resources
- Character encodings that cause database issues
- Inputs that bypass business logic (Google Developers, n.d.)

The Australian Cyber Security Centre (ACSC) emphasizes the importance of input validation as a critical defence against web application vulnerabilities. In their annual reports, they highlight that input validation failures are a common vector for cyber threats, underscoring the need for robust validation mechanisms in application development (ACSC, 2023).

### Limitations of Existing Solutions

While many security approaches exist, most implementations suffer from significant limitations:

**Single-Layer Approaches**: Relying solely on CAPTCHA or similar single-layer validation methods can leave applications vulnerable to sophisticated bots that can bypass these mechanisms (Imperva, 2024).

**User Experience Trade-offs**: Traditional solutions like CAPTCHA can create friction for users, potentially decreasing form completion rates. For instance, the implementation of CAPTCHA challenges can lead to user frustration and abandonment of forms (Google Developers, n.d.).

**Exclusive Focus on Client-Side Validation**: Implementing validation exclusively on the client side can be easily bypassed by attackers, as client-side scripts can be manipulated or disabled, allowing malicious inputs to reach the server (ACSC, 2023).

**Honeypot-Only Solutions**: While honeypots can deter basic bots, they are often ineffective against more advanced, AI-driven bot attacks. Sophisticated bots can detect and avoid honeypot fields, rendering this method insufficient when used in isolation (Imperva, 2024).

## 4. Our Solution: Multi-Layered Security Implementation

This project implements a comprehensive multi-layered defence strategy that improves upon existing approaches while maintaining excellent user experience:

### 1. Client-Side Validation (Frontend JavaScript)

Our implementation begins with immediate user feedback through progressive form validation:

```javascript
// Real-time validation as users interact with the form
input.addEventListener("blur", () => {
  validateField(input);
  updateFormStatus();
});

// Clear errors as users correct their input
input.addEventListener("input", () => {
  input.classList.remove("error-field");
  document.getElementById(`${input.id}-error`).textContent = "";
  updateFormStatus();
});
```

This provides instant feedback without requiring server round-trips, enhancing user experience while still maintaining security.

### 2. Honeypot Traps for Bot Detection

We implement an invisible field that only bots would complete, using more sophisticated CSS-based hiding that's resistant to detection:

```javascript
// Server-side honeypot validation
body("honeypot").custom((value) => {
  if (value) throw new Error("Bot detected via honeypot field.");
  return true;
}),
```

This technique exploits the behaviour of most bots, which automatically fill all available fields. Humans won't see or interact with this field, but bots typically complete it, allowing us to identify and block automated submissions.

### 3. Time-Based Validation

A separate security layer checks submission timing to identify automated submissions:

```javascript
// Client-side timestamp generation when form loads
document.getElementById("form_timestamp").value = Date.now();

// Server-side time-based validation
body("form_timestamp").custom((value) => {
  const submittedAt = parseInt(value, 10);
  const now = Date.now();

  if (!submittedAt || isNaN(submittedAt)) {
    throw new Error("Missing or invalid timestamp.");
  }

  if (now - submittedAt < MIN_TIME_MS) {
    throw new Error("Form submitted too quickly. Possible bot.");
  }
  
  if (now - submittedAt > MAX_TIME_MS) {
    throw new Error("Form expired. Please refresh the page and try again.");
  }

  return true;
}),
```

This validation ensures that submissions occur within a reasonable timeframe. Forms submitted in less than 3 seconds are flagged as potential bots, while forms older than 1 hour are rejected to prevent replay attacks.

### 4. Rate Limiting

We restrict the number of submissions from a single IP address using Express middleware:

```javascript
// Rate limiting middleware: max 5 submissions per IP per minute
const contactLimiter = rateLimit({
  windowMs: 60 * 1000,
  max: 5,
  message: "Too many contact form submissions. Please try again later.",
});
```

This prevents flooding attacks while allowing legitimate users to submit forms without interruption.

### 5. Robust Server-Side Validation

The final security layer implements comprehensive validation rules for all form fields:

```javascript
// First name validation
body("first_name")
  .trim()
  .notEmpty().withMessage("First name is required.")
  .isLength({ max: 50 }).withMessage("First name cannot exceed 50 characters.")
  .matches(/^[A-Za-z\s\-'.]+$/).withMessage("First name contains invalid characters."),

// Email validation with normalisation
body("email")
  .trim()
  .notEmpty().withMessage("Email is required.")
  .isEmail().withMessage("Please enter a valid email address.")
  .normalizeEmail()
  .isLength({ max: 100 }).withMessage("Email is too long."),

// Message validation with length constraints
body("message")
  .trim()
  .notEmpty().withMessage("Message is required.")
  .isLength({ min: 5 }).withMessage("Message must be at least 5 characters.")
  .isLength({ max: 2000 }).withMessage("Message cannot exceed 2000 characters."),
```

Each field undergoes strict validation with appropriate error messaging, preventing malformed data from entering the system. To ensure consistency between client and server validation, we enforce a minimum message length of 5 characters on the server, matching our client-side validation requirement.

### 6. Structured Route Implementation

Our Express router implements the security layers in a strategic sequence:

```javascript
// POST route with middleware chain
router.post("/", contactLimiter, validateContactForm, handleContact);
```

This ensures each submission is checked for rate limiting, then validated through our comprehensive rules, and only then processed by the application controller.

### 7. Comprehensive Error Handling

The frontend provides detailed feedback to legitimate users while revealing minimal information to potential attackers:

```javascript
// Map server validation errors back to form fields
result.errors.forEach(error => {
  const fieldName = error.path;
  const field = document.getElementById(fieldName);

  if (field) {
    field.classList.add("error-field");
    const errorSpan = document.getElementById(`${fieldName}-error`);
    if (errorSpan) {
      errorSpan.textContent = error.msg;
    }
  }
});

// Special handling for security-related errors
const botError = result.errors.find(
  err => err.path === "honeypot" || err.path === "form_timestamp"
);

responseDiv.textContent = botError
  ? "Submission blocked: Possible bot detected."
  : "Oops! Please correct the highlighted fields in red before submitting.";
```

This maintains a positive user experience while still implementing robust security measures.

### Why This Multi-Layered Approach Works

Our implementation follows the security principle of defence in depth, with multiple independent layers of protection:

1. Browser's built-in validation - First line of defence
2. Client-side JavaScript validation - Immediate user feedback
3. Honeypot traps - Bot detection through hidden fields
4. Time-based checks - Separate mechanism to detect submissions that are too quick
5. Rate limiting - Prevents flooding and DDoS attempts
6. Server-side validation - Final authoritative check

Implementing a multi-layered security approach greatly strengthens protection against spam and phishing. A study in Computers & Security found that combining content filtering with behavioural analysis reduced false negatives by up to 55 percent (Zhou & Zhang, 2023). Similarly, research from the Future Technologies Conference 2024 showed that multi-factor authentication lowered unauthorized access risks by over 99.99 percent (Muir, Brown & Girma, 2024). These results support using layered defences such as CAPTCHA, honeypots, rate limiting, and server-side validation. If one measure fails, others remain in place. Unlike many tutorials that rely on a single technique, our modular and well-documented approach combines multiple methods to improve security without sacrificing usability.

## 5. Project Implementation Plan

The implementation of this secure contact form followed a structured, efficient approach to create a focused demonstration of multi-layered security which you can follow or tweak. Throughout the development process, I employed atomic commits with proper commit conventions to maintain a clean, traceable development history.

### Phase 1: Research and Planning (1 day)

**Morning: Security Research & Requirements (3 hours)**
- Review latest form security guidelines and best practices
- Study common form attack patterns from security reports
- Define security requirements and acceptance criteria
- Create project repository with appropriate structure

**Afternoon: Technology Selection & Setup (3 hours)**
- Evaluate and select appropriate technology stack
- Compare security libraries and validation approaches
- Set up development environment with necessary dependencies
- Draft project structure following best practices

### Phase 2: Basic Implementation (1 day)

**Morning: Frontend Foundation (3 hours)**
- Create HTML structure for the contact form with accessibility in mind
- Implement responsive CSS design using modern layouts
- Set up form fields with appropriate input types
- Add basic styling for visual appeal and usability

**Afternoon: Backend Foundation (3 hours)**
- Initialise Express.js application with core middleware
- Create route handlers for form submission endpoint
- Implement basic controller logic for processing submissions
- Set up project folder structure and configuration

### Phase 3: Security Implementation (2 days)

**Day 1: Client-Side Security (6 hours)**
- Implement real-time validation feedback for form fields
- Create client-side timestamp generation for time-based validation
- Add form submission handling via fetch API
- Implement honeypot field with CSS-based hiding
- Create visual feedback for validation states

**Day 2: Server-Side Security (6 hours)**
- Implement Express-Validator middleware with comprehensive validation rules
- Create honeypot validation logic on server side
- Develop time-based validation with appropriate thresholds
- Set up rate limiting middleware to prevent flooding
- Implement error handling and appropriate security responses

### Phase 4: Testing and Refinement (1 day)

**Morning: Testing (3 hours)**
- Test form against common bot patterns using Insomnia REST client
- Validate security measures by triggering each protection mechanism
- Test across different browsers and device sizes
- Identify and document any security gaps

**Afternoon: Refinement (3 hours)**
- Refine validation rules based on testing results
- Optimise error messaging for clarity and helpfulness
- Adjust security thresholds for optimal balance
- Enhance styling and user experience elements

### Phase 5: Documentation and Finalisation (1 day)

**Morning: Code Documentation (3 hours)**
- Add comprehensive comments to all security-related code
- Document security implementation details in README.md
- Create installation and usage instructions
- Include package version information and dependencies

**Afternoon: Final Repository Setup (3 hours)**
- Finalise README with comprehensive security implementation overview for users to integrate these security measures into their own contact forms
- Develop demonstration materials such as screenshots and code snippets, highlighting each security feature and its effectiveness against common attack vectors

## 6. Skills Required and Justified

This project is a prototype (MVP) demonstrating a secure contact form built with a focus on usability, performance, and layered security. The technology stack was deliberately kept lightweight and consistent to support rapid development and ease of maintenance.

### Frontend Development Skills

#### HTML/CSS
- Semantic HTML structure improves accessibility and SEO
- CSS enables responsive design and immediate visual feedback
- Form usability patterns enhance interaction clarity

While frameworks like React or Vue could provide component-based architecture for more complex forms, plain HTML and CSS were chosen for this MVP to eliminate unnecessary complexity and dependencies. This approach ensures broader compatibility and easier implementation for developers focusing on security rather than advanced UI features. These skills were essential for designing an interface that balanced security and user-friendliness.

#### JavaScript
JavaScript is essential for implementing dynamic, real-time form interactions and enhancing the user experience. It enabled:

- DOM manipulation for inline error messaging and visual feedback
- Event handling to validate inputs as users type or submit the form
- Asynchronous submissions using the Fetch API to send form data without reloading the page
- Time-based validation by capturing timestamps at page load and form submission to detect automated bots
- Client-side honeypot checking, providing an early layer of spam detection before requests reach the server

While client-side validation alone is not secure, it improves usability by catching basic input errors early and reducing unnecessary server requests. According to MDN, client-side validation is recommended for improving user experience, though it must be backed by robust server-side checks to ensure complete security (MDN, n.d.).

This layered use of JavaScript complements backend measures like rate limiting and server-side validation, helping to create a responsive and secure contact form without overwhelming the user.

### Backend Development Skills

#### Node.js / Express
- RESTful API routing for handling contact form submissions
- Middleware implementation (e.g., validation, rate limiting)
- Centralised error handling and clean response formatting
- Security-conscious architecture using Express extensions

Node.js was chosen for its non-blocking I/O model, ideal for handling concurrent spam attempts or high-volume submissions. Express offered a modular framework to layer validation and throttling efficiently.

### Security Knowledge
- Understanding of common attack vectors and bot behaviour patterns
- Implementation of defence-in-depth strategies through modular middleware
- Rate limiting and throttling techniques to prevent flooding attacks
- Input validation and sanitisation to prevent injection attacks

The implementation of three distinct security methods—honeypot fields, time-based validation, and rate limiting—was chosen over simpler single-method approaches. Next, the time-based validation in this project uses a hybrid client-server approach where the timestamp is generated client-side (via JavaScript's Date.now()) but validated server-side against configurable time constraints. This architecture was specifically chosen over server-only approaches because it allows detection of submissions that occur too quickly to be human (less than 3 seconds) while still keeping the validation logic secure on the server. This is more effective than traditional honeypots alone because it catches bots that might avoid filling hidden fields but still submit forms at inhuman speeds.

This multi-layered approach follows the principle of defence in depth, ensuring that if one security measure is bypassed, others remain in place to provide continued protection. Separating concerns, such as isolating validation and rate limiting into dedicated middleware files like validation.js and rateLimiter.js, reflects best practices in secure and maintainable architecture.

### Alternative Technologies Considered

#### Flask vs. Node.js

Flask (Python) was considered but ultimately not selected. Node.js was more appropriate for this MVP due to:

- **Single language stack**: Using JavaScript across both frontend and backend reduced context switching, enabling faster prototyping and easier maintenance
- **Asynchronous performance**: Node's event-driven architecture efficiently manages high traffic and bot submissions
- **Security ecosystem**: Middleware like express-rate-limit and express-validator allowed quick implementation of the modular security architecture (controllers, middleware, routes)

While Flask is excellent for API-driven Python projects, Node.js offered greater consistency and speed for building this full-stack prototype.

#### React vs. Vanilla JavaScript

Although React offers powerful features like reusable components, built-in state management, and developer tooling, it was intentionally not used in this MVP. Instead, vanilla JavaScript was chosen to:

- Eliminate the overhead of additional dependencies
- Minimise security risks from third-party libraries
- Maintain a lightweight, fast-loading client experience
- Ensure broader browser compatibility and fewer build steps

For a focused, single-form application, vanilla JavaScript simplifies implementation while still supporting interactive validation, dynamic feedback, and asynchronous submission. This approach prioritises performance and security over UI complexity—ideal for a minimal, secure proof of concept.

#### Joi vs. Express-Validator

Both libraries are widely used for server-side validation, but Express-Validator was selected for this project due to:

- Seamless integration with Express middleware chains
- A minimal learning curve with strong support for both standard and custom validations
- Built-in support for chaining validation and sanitisation methods
- Flexibility to implement honeypot fields and time-based bot detection directly in middleware

This decision allowed for concise, maintainable code that aligns with Express architecture. By separating validation logic into validation.js and request throttling into rateLimiter.js, the project adheres to best practices in modular security design—ensuring it can evolve as security needs grow.

## 7. Lessons Learned and Future Improvements

### Skills Gained Throughout This Project

This project significantly expanded my technical capabilities and knowledge in several key areas:

1. **Advanced JavaScript Security Techniques**: I developed skills in implementing time-based validation and honeypot fields, gaining practical experience with anti-automation security measures beyond basic form validation.
2. **Modular Backend Architecture**: I learned to structure Express.js applications with separate concerns (controllers, routes, middleware) to create maintainable and secure code.
3. **Client-Server Security Coordination**: I gained expertise in coordinating security measures across both client and server sides, understanding how timestamp generation on the client and validation on the server work together.
4. **Error Handling Strategies**: I developed more sophisticated approaches to error handling, particularly in mapping server-side validation errors back to client-side form fields for improved user feedback.
5. **Security-Focused Testing**: I learned methodologies for testing security measures by intentionally triggering different security defences to verify their effectiveness.

### Key Lessons Beyond Technical Skills

The development process provided valuable insights beyond code:

1. **Security is multi-layered**: No single security measure is sufficient. The combination of honeypots, time-based validation, rate limiting, and input validation creates a more robust system than any individual approach.
2. **User experience must be balanced with security**: Overly restrictive validation (like requiring exactly-formatted phone numbers) can frustrate users and reduce form completion rates.
3. **Server-side validation is non-negotiable**: While client-side validation improves user experience, it can be bypassed. Server-side validation provides the authoritative security check.
4. **Feedback clarity impacts security perception**: Clear, specific error messages not only help users complete forms but also build trust in the security of the system.

### Challenges Faced

Several significant challenges emerged during development:

1. **Balancing strictness in name validation**: Initial validation was too strict, rejecting valid cultural variations of names. This highlighted the importance of inclusive validation patterns. I addressed this by expanding the character set allowed in names to include apostrophes, hyphens, and periods.
2. **Time-based detection calibration**: Setting realistic minimum and maximum time thresholds was challenging, as there is no universal standard for how long a human takes to complete a form. For example, during testing, setting the minimum time to 30 seconds caused real users to be incorrectly flagged as bots. Debugging involved logging the time difference between form load and submission, revealing that most users submitted within 5 seconds. This insight helped calibrate the thresholds to better balance security and usability.
3. **Error propagation from server to client**: Mapping server-side validation errors back to specific form fields required careful coordination between frontend and backend code. This was one of the most technically challenging aspects of the project, requiring multiple iterations to get right.

### What Could Be Done Differently

If addressing this problem again, I would approach several aspects differently:

1. **Start with automated testing**: Building security-focused tests first would have saved time by catching edge cases earlier in development.
2. **Use TypeScript instead of JavaScript**: Type safety would have prevented several subtle bugs in error handling and data validation.
3. **Consider a more robust frontend framework**: While vanilla JavaScript was suitable for this prototype, a framework like React would offer better state management for more complex forms.

### Intentionally Unfinished Components

Certain features were deliberately left unimplemented in this prototype:

1. **Persistent data storage**: This prototype intentionally lacks database integration or JSON storage for form submissions. In a production environment, submissions would be stored securely, but for demonstration purposes, submissions are only logged to the console. This simplified approach keeps the focus on security implementation while avoiding unnecessary complexity.
2. **Email notification system**: A production contact form would send notifications to administrators when submissions are received. This feature was omitted to keep the prototype focused on core security concepts.
3. **Admin interface**: A real-world implementation would include an administrative panel to review submissions. This was deemed out of scope for the security-focused prototype.

### Future Improvements

Given more time and resources, several improvements could enhance this implementation:

1. **Machine learning-based bot detection**: Implementing behavioural analysis to detect patterns associated with automated submissions, particularly targeting sophisticated AI-generated spam.
2. **Progressive enhancement for older browsers**: Adding fallbacks for browsers that don't support modern JavaScript features.
3. **Internationalisation support**: Expanding validation to handle international character sets and multilingual error messages.
4. **Advanced analytics**: Adding monitoring to track submission patterns and automatically adjust security thresholds.
5. **Email verification step**: Implementing a double opt-in process for higher-security applications.

These future enhancements would build upon the solid security foundation established in this prototype, addressing more advanced threat scenarios while further improving user experience.

## Conclusion

This secure contact form project demonstrates a comprehensive approach to form security that balances robust protection with a positive user experience. By layering defences, including honeypots, time-based validation, rate limiting, and input sanitisation, it ensures a higher level of security while minimising friction for users. This multi-layered strategy effectively mitigates bot attacks and spam submissions, while safeguarding against malicious inputs. The result is a user-friendly yet highly secure contact form that aligns with modern best practices and can be adapted to a variety of real-world applications.

Through thoughtful planning, clear technology choices, and intentional implementation, this project delivers a working prototype that can be adapted to many real-world use cases requiring secure user input.

### What's Next

This resource was created to support developers—whether experienced or just starting out—in building secure contact forms from scratch without relying on third-party form handlers. You can explore the full implementation, including complete code examples and setup instructions, on the GitHub repository:

GitHub.com/Donjella/secure-contact-form

### Customising for Your Needs

The project is designed to be easily customisable:

- **Time-based validation**: Adjust the MIN_TIME_MS and MAX_TIME_MS constants in validation.js to fine-tune bot detection sensitivity
- **Rate limiting**: Modify the submission limit (max) and time window (windowMs) in rateLimiter.js to match your application's traffic patterns
- **Validation rules**: Customise field validation in validation.js to match your form's specific requirements
- **Styling**: Adapt the CSS to match your website's design system

While the honeypot implementation itself is relatively standard (a hidden input field that should remain empty), its placement and styling can be adjusted to make it less detectable by sophisticated bots.

### Implementation Tips

For the best results when implementing this solution:

1. Always maintain all three security layers (honeypot, time-based validation, and rate limiting)
2. Test your form against automated submission tools before deployment
3. Monitor submission patterns to identify and adapt to new attack vectors

As AI-powered bots grow more sophisticated, secure form design will remain an ongoing challenge that demands continuous improvement. By building on this foundation and tailoring it to your specific needs, you can create a contact form that effectively protects against spam while delivering a seamless experience for legitimate users.

## References

ACSC (2023) Annual Cyber Threat Report July 2022 to June 2023, Australian Cyber Security Centre, viewed 20 April 2025, https://www.cyber.gov.au/sites/default/files/2023-11/asd-cyber-threat-report-2023.pdf.

Ellis, C. & Brandl, R. (2024) Spam Statistics 2025: New Data on Junk Email, AI Scams & Phishing, EmailToolTester, 16 October, viewed 20 April 2025, https://www.emailtooltester.com/en/blog/spam-statistics/.

Falokun, C. (2025) How AI is Fueling ATOs & Fake Account Creation—And Why Bot Detection Needs to Evolve, DataDome, 26 March, viewed 20 April 2025, https://datadome.co/bot-management-protection/how-ai-is-fueling-atos-and-fake-account-creation-and-why-bot-detection-needs-to-evolve/.

Formsort (2023) Key Form Completion Stats, viewed 20 April 2025, https://formsort.com/article/key-form-completion-stats/.

Google Developers (n.d.) Avoiding Common Mistakes with reCAPTCHA, viewed 20 April 2025, https://developers.google.com/recaptcha/docs/analytics.

Imperva (2024) What is a Honeypot, viewed 20 April 2025, https://www.imperva.com/learn/application-security/honeypot-honeynet/.

Law, D. (2025) AI Spam Statistics in Australia, Red Search, 22 January, viewed 20 April 2025, https://www.redsearch.com.au/resources/ai-spam-statistics-australia/.

MDN (n.d.) Client-side form validation, Mozilla Developer Network, viewed 20 April 2025, https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation.

Muir, A., Brown, K. & Girma, A. (2024) 'Reviewing the Effectiveness of Multi-factor Authentication (MFA) Methods in Preventing Phishing Attacks', Future Technologies Conference 2024, Springer, pp. 597–607, viewed 20 April 2025, https://link.springer.com/chapter/10.1007/978-3-031-73128-0_40.

Office of the Australian Information Commissioner (OAIC) (2019) Chapter 11: APP 11 — Security of personal information, viewed 20 April 2025, https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-guidelines/chapter-11-app-11-security-of-personal-information.

Stanford Institute for Human-Centered AI (2023) AI-Detectors Biased Against Non-Native English Writers, Stanford University, 15 May, viewed 20 April 2025, https://hai.stanford.edu/news/ai-detectors-biased-against-non-native-english-writers.

Umapathy, G.V. (2024) How Multifactor Authentication Strengthens Remote Access Security, Zscaler, 12 December, viewed 20 April 2025, https://www.zscaler.com/blogs/product-insights/how-multifactor-authentication-strengthens-remote-access-security.

Veracode (2024) State of Software Security 2024: Addressing the Threat of Security Debt, viewed 20 April 2025, https://www.veracode.com/state-software-security-2024-report.

W3C Web Accessibility Initiative (n.d.) Security and Accessibility, World Wide Web Consortium, viewed 20 April 2025, https://www.w3.org/WAI/APA/wiki/Security_and_accessibility.

Winder, D. (2020) 'Phishing Warning: 25% Of All Emails Claiming To Be From Apple Are Scams', Forbes, 8 July, viewed 20 April 2025, https://www.forbes.com/sites/davewinder/2020/07/08/phishing-warning-25-of-all-emails-claiming-to-be-from-apple-are-scams/.

Zhou, Y. & Zhang, X. (2023) 'A comprehensive dual-layer architecture for phishing and spam email detection', Computers & Security, vol. 123, 102931, viewed 20 April 2025, https://www.sciencedirect.com/science/article/pii/S0167404823002882.