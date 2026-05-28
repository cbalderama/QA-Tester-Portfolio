# QA Tester Portfolio

## About Me

Software Quality Test Engineer with 4+ years across finance, healthcare, AI, and tourism. I architect testing strategies that prevent bugs before they reach production.

**Key Results:**
- Above 85% code coverage (Jest tests) — exceeded 80% target
- 100% test execution rate across 5 major projects
- 30-day timeline acceleration through optimized test planning
- 87% automation framework coverage

---
To demonstrate my capabilities as a Software Test Engineer, I have developed a sample E-commerce App that will be the subject of the following test documents  

## TEST DOCUMENTATION SAMPLES
### Test Plan: E-Commerce Mobile App
**Project Overview:** React Native Expo app with Firebase backend and GitHub Actions CI/CD pipeline

**Key Sections:**
- 150+ test cases across 7 modules (authentication, cart, checkout, wishlist, orders, profile, search)
- Testing levels: Unit (86.55% coverage), Integration, System, Acceptance, Regression
- Entry/Exit criteria with quality gates (80% coverage, 0 P0 defects, SonarCloud passing)
- Risk assessment and defect management (P0-P3 severity levels)
- Automation strategy: Jest unit tests, CI/CD pipeline, EAS mobile builds

[Full Test Plan](https://drive.google.com/file/d/1McHX65oCx7CPRiYcl4Q3pblZZE2R3XAY/view?usp=sharing)

---

### Test Execution Report: Sprint 12
**Results:** 2 test cases executed | 1 PASSED ✅ | 1 FAILED ❌

**Critical Finding:**
- **TC-CART-001** (Add to Cart) — ✅ PASSED
  - Successfully added product, updated quantity, verified Firebase persistence  
  - [Test Case](https://drive.google.com/file/d/1XjJ8XYJlEDDNHN8ilfJlPwJM-GAKV2WY/view?usp=sharing)  
  - [Test Evidences](https://drive.google.com/drive/folders/18WYtXKNZLO8XtADyB7XACXH7yC3YT1Tt?usp=sharing)
    
- **TC-ORDER-001** (Checkout) — ❌ FAILED
  - **Defect DEF-2026-001:** Order visible in UI but not persisted to Firebase
  - Impact: BLOCKS PRODUCTION (affects 100% of checkout users)  
    [Test Case](https://drive.google.com/file/d/1ZF_pcjgQBcx--u1_phpu5P6nnreOFl5I/view?usp=sharing)  
    [Test Evidences](https://drive.google.com/drive/folders/18ERWoZmy9JnnWn-maOCZCezyk1kGjMFi?usp=sharing)  

---

### Unit Testing: 86.55% Coverage Achievement

**Framework:** Jest + TypeScript  
**Total Tests:** 49 | **Pass Rate:** 100%

**Coverage by Service:**

| Service | Coverage | Tests | Achievement |
|---------|----------|-------|-------------|
| products.ts | 100% | 18 | Perfect coverage |
| wishlist.ts | 92.3% | 11 | Excellent |
| cart.ts | 78.26% | 20 | Good |
| orders.ts | 74% | 5 | Fair |

**Code Sample - Happy Path:**
```typescript
it('should calculate cart total correctly', () => {
  const items = [
    { product: { price: 10 }, quantity: 2 },
    { product: { price: 20 }, quantity: 1 }
  ];
  expect(calculateCartTotal(items)).toBe(40);
});
```

**Code Sample - Error Handling:**
```typescript
it('should handle Firebase errors gracefully', async () => {
  mockGetDocs.mockRejectedValue(new Error('Firebase error'));
  await expect(getCartItems('user123')).rejects.toThrow();
});
```

**Key Challenges Solved:**
1. Jest 30 + ts-jest 29 incompatibility → Downgraded to Jest 29
2. Empty mock data not increasing coverage → Rewrote with realistic test data
3. CodeQL false positives on coverage reports → Excluded coverage/ directory
4. ESLint react-hooks/exhaustive-deps violations → Wrapped async functions with useCallback

 [Unit Testing Report](https://drive.google.com/file/d/1qJr_jHLfjji2EdBnV6SH-ECrpJkS0Pgc/view?usp=sharing) 

---


### CI/CD Pipeline (GitHub Actions)

**Automated Checks on Every PR:**
1. ESLint → Code style validation ✅
2. TypeScript → Type checking ✅
3. Jest → Unit tests (49 tests) ✅
4. SonarCloud → Quality gate (86.55% coverage) ✅
5. CodeQL → Security scanning ✅

**Pipeline Status:**
- ✅ CI passing 100%
- ✅ SonarCloud Quality Gate: PASSED
- ✅ CodeQL: 0 vulnerabilities

[View GitHub Actions](https://github.com/cbalderama/PersonalProject/actions)

---

##  METRICS & RESULTS

### Code Coverage Dashboard

| Metric | Result | Target | Status |
|--------|--------|--------|--------|
| Overall Coverage | 86.55% | ≥ 80% | ✅ EXCEEDED |
| Functions | 89.18% | ≥ 80% | ✅ EXCEEDED |
| Lines | 84.68% | ≥ 80% | ✅ EXCEEDED |
| Test Cases | 49 | - | ✅ COMPREHENSIVE |

### Quality Gates

| Check | Status | Details |
|-------|--------|---------|
| SonarCloud | ✅ PASSED | 0 code smells, 0 vulnerabilities |
| CodeQL | ✅ PASSED | 0 high/critical security issues |
| Test Execution | ✅ 100% | All 49 tests passing |
| CI Pipeline | ✅ 100% | All checks passing |

---

## Tech Stack

**Testing:** Jest • Selenium • Appium • Postman  
**CI/CD:** GitHub Actions • SonarCloud • CodeQL  
**Languages:** JavaScript • TypeScript • Java • SQL  
**Tools:** JIRA • Qtest • Git • Firebase

---

##  Resources

- **GitHub Profile:** [cbalderama](https://github.com/cbalderama)
- **Main Project:** [PersonalProject](https://github.com/cbalderama/PersonalProject)
- **Code Quality:** [SonarCloud Dashboard](https://sonarcloud.io/summary/new_code?id=cbalderama_PersonalProject)
- **LinkedIn:** [cydrick-balderama](https://www.linkedin.com/in/cydrick-balderama-91953a21b)
- **Email:** devbalderama@gmail.com

