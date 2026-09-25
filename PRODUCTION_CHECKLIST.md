# Family Calendar — Production Checklist

## 1. Local MVP (completed in v3)
- Monthly budget total
- Category allocations
- Items under categories
- Planned / Actual / Remaining
- Execution Status
- Recurring flag
- Calendar status
- Shopping list

## 2. Firebase setup (next developer step)
1. Create a Firebase project named `Family Calendar`.
2. Add Android app package: `com.familycalendar.app`.
3. Download `google-services.json` and place it in `app/`.
4. Enable Authentication: Google + Email/Password.
5. Create Firestore Database.
6. Add App Check after the first internal build is working.
7. Create these collections:
   - users/{uid}
   - families/{familyId}
   - families/{familyId}/members/{uid}
   - families/{familyId}/events/{eventId}
   - families/{familyId}/budgets/{yyyy-MM}
   - families/{familyId}/categories/{categoryId}
   - families/{familyId}/categories/{categoryId}/items/{itemId}
   - families/{familyId}/shopping/{itemId}
   - families/{familyId}/reminders/{reminderId}
8. Firestore security rules must restrict every family document to authenticated members of that family.

## 3. Production data model
A budget month is identified by `yyyy-MM`.
Each category has a planned budget. Each item has planned and actual values. Actual spending must be stored as transactions rather than only overwriting an aggregate.

Recommended transaction fields:
- id
- familyId
- month
- categoryId
- itemId
- amount
- date
- note
- createdBy
- createdAt
- recurringSourceId (nullable)

## 4. Account and privacy
- Sign in / sign out
- Create family
- Join family with invitation code
- Remove member
- Delete account
- Delete family data where the user is the owner
- Privacy Policy screen
- Terms screen
- Data deletion request flow

## 5. Notifications
- Event reminders
- Recurring expense reminders
- Budget threshold alerts at 75%, 90%, 100%
- Monthly report notification

## 6. Monetization
Free:
- Core calendar
- Basic budget
- Shopping list
- Limited family members
- Ads

Premium:
- No ads
- Unlimited family members
- Advanced reports
- Unlimited categories/items
- Cloud backup/history
- Advanced budget alerts

Use Google Play Billing for subscriptions. Use AdMob for ads. Never hard-code production ad IDs in debug builds.

## 7. Play release
- Unique application ID
- Version code incremented on every release
- Target API 36+
- Release signing / Play App Signing
- Privacy Policy URL
- Data Safety form
- Content rating
- Target audience declaration
- App access instructions if login is required
- Store icon
- Feature graphic
- Screenshots
- Arabic + English store listing
- Closed testing when required by the developer account
- Production release

## 8. Launch metrics
Track:
- Installs
- Sign-up conversion
- Families created
- D1 / D7 / D30 retention
- Monthly active families
- Budget created per family
- Expenses entered per active family
- Premium conversion
- Ad revenue per active user
- Crash-free users

## 9. Important rule
Do not publish the demo-data version as the final product. The production release must use authenticated cloud data, real notifications, real account deletion, production privacy documents, and verified monetization flows.
