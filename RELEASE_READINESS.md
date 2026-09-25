# Family Calendar V4 — Release Readiness

## Product scope
- Family Calendar dashboard
- Family members
- Calendar events + Execution Status
- Monthly Budget Planning
- Categories and nested budget items
- Planned / Actual / Remaining / Execution %
- Recurring expenses
- Shopping list
- Reminders
- Premium concept screen
- Arabic RTL UI
- Local persistence for budget categories and shopping list
- Android target API 36

## Important V4 limitation
V4 is a release-candidate prototype, not a store-ready cloud production app yet. Before public release, replace local-only storage with authenticated cloud sync, implement real account deletion, real notifications, production-grade calendar CRUD, AdMob consent/integration, Google Play Billing, privacy policy hosting, Data Safety declarations, analytics, crash reporting, and signed AAB release configuration.

## Definition of done before Play production
- [ ] Firebase/Auth + Family invite/join
- [ ] Cloud database + security rules
- [ ] Month-specific budgets/expenses
- [ ] Real event create/edit/delete
- [ ] Real recurring events/expenses
- [ ] Android notifications
- [ ] Delete account/data
- [ ] Privacy Policy URL
- [ ] Data Safety completed accurately
- [ ] AdMob production IDs + consent flow
- [ ] Play Billing Premium
- [ ] Signed AAB + Play App Signing
- [ ] Closed test if required by account
- [ ] Store listing + screenshots + feature graphic
- [ ] Production review
