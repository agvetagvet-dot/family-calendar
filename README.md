# Family Calendar — MVP v2

Android app concept for family calendar, reminders, shopping and monthly budget planning/execution.

## Included in v2
- Family Calendar branding and onboarding
- Home dashboard
- Family members
- Calendar events with Execution Status: مخطط / قيد التنفيذ / تم
- Expenses redesigned as Plan → Execute → Track
- Monthly budget summary: Plan / Actual / Remaining / Execution %
- Expense categories: Food, Education, Healthcare, Entertainment, Sports, Savings, Transportation, Bills
- Category-level budgets
- Item-level planned and actual amounts
- Item execution status derived from actual vs planned
- Recurring expense flag
- Add category and add budget item dialogs
- Expandable categories and progress indicators
- Shopping list with check-off and delete
- Local persistence using SharedPreferences/JSON for categories and shopping list
- Premium placeholder screen
- Arabic RTL interface
- compileSdk/targetSdk 36

## Example Education hierarchy
Education
- School tuition
- Private lessons
- Transportation
- External books
- School supplies

## Important next production phases
1. Replace demo data with Room database and month-specific records.
2. Add user/family accounts and cloud sync (Firebase/Supabase).
3. Add real calendar event creation/editing and Android notifications.
4. Add recurring bills and recurring events.
5. Add charts and monthly reports.
6. Add AdMob.
7. Add Google Play Billing for Premium.
8. Add privacy policy, consent, data safety form and production signing.
9. Build signed AAB and complete Play Console testing/release.

This repository is an MVP source project; the build environment must have Android SDK/API 36 and Gradle/Android Gradle Plugin dependencies installed to produce an APK/AAB.

## v3 foundation changes
- Added a separately stored monthly budget total.
- Category budgets are allocations from the monthly budget; adding an item no longer silently increases the category budget.
- Added monthly budget edit flow and unallocated-budget visibility.
- Added explicit item Execution Status selection: مخطط / قيد التنفيذ / تم.
- Item rows now show planned, actual, remaining, progress and a full-completion action.
- Added a production roadmap for cloud sync, authentication, notifications, monetization and Play release.
