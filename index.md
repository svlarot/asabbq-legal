# ASA BBQ Privacy Policy

**Last updated: 14 May 2026**

This page explains what the ASA BBQ customer mobile app does with your information. We've kept it short and in plain English, because most privacy policies are neither. If anything below isn't clear, write to us at **support@bluenex.org** and we'll explain.

This policy covers the ASA BBQ customer app, distributed on the Google Play Store under the package name `com.asabbq.customer_mobile`. ASA BBQ is a restaurant in **Bogo City, Cebu, Philippines**. The app is the customer-facing companion to the restaurant — it shows our menu, lets you place an order for dine-in or pick-up, and tracks the status of that order.

---

## The short version

- The app is a menu and ordering companion for our restaurant. The things you put into it — your cart, your order, your contact name — are tied to your account so we can prepare your food and follow up if something goes wrong.
- You don't need to make an account just to browse the menu. The app signs you in anonymously on first launch so the menu can load. You only need to sign in with Google when you're about to place an order, so your order history can follow you between phones.
- We do **not** take card or bank details inside the app. Paid orders are settled by GCash (a Philippine e-wallet), using a QR code shown by the app. You confirm the payment yourself by entering the GCash reference number.
- The app shows a small banner ad supplied by Google AdMob. AdMob may collect advertising identifiers and similar data per Google's own policies.
- We do not sell your data. We do not share it with advertisers beyond what Google AdMob itself collects.
- You can ask us to delete your account and order history at any time. See the [account-deletion page](./delete-account/) for the step-by-step.
- We do not currently use any third-party analytics or crash-reporting service.

---

## What we collect

We collect what you give us, plus the small amount of information that's required to run the app safely.

### Information you give us

- **Google account details (only when you sign in at checkout).** When you're ready to place an order, the app asks you to sign in with your Google account. Through Google, we receive your name, email address, profile picture link, and a stable Google account ID. We use these so your order history follows you between phones, and so we can contact you about a specific order.
- **Order details.** Items in your cart, the totals, options or notes you add to an item, the table you are seated at (if applicable), and the order type (dine-in, pick-up). When you submit the order it is saved to your account on our backend.
- **GCash reference number.** For orders paid through GCash, you enter the reference number shown to you by the GCash app after you've sent payment. That reference is stored against the order so our staff can match the payment.

### Information collected automatically

- **Authentication metadata.** Sign-in timestamps, refresh tokens, and the IP address of the device making each authentication request. This is standard for our authentication provider (Supabase Auth, also known as GoTrue) and is used to keep your session valid and to protect your account from unauthorised access.
- **Anonymous user ID.** On first launch, before you sign in with Google, the app creates an anonymous account so the menu can load and you can build a cart. This account is just a randomly generated identifier — it has no email or name attached to it. When you later sign in with Google, the anonymous account is linked to your Google identity so the same user ID is preserved.
- **Device identifiers (because the home screen shows an ad).** The Google Mobile Ads SDK and Google's User Messaging Platform (UMP) receive your device's advertising ID and similar signals when the banner loads. See [Google's privacy policy](https://policies.google.com/privacy) for the details of what Google collects.

### Information we do not collect

- We do **not** request access to your contacts, SMS, call log, microphone, camera, photos, or precise location.
- We do **not** ask for, see, or store your card number, bank account number, GCash PIN, or GCash login. The only payment information that touches our servers is the reference number you copy in after paying through GCash directly.
- We do **not** collect biometric data.

---

## What stays on your device

Some things never leave your phone:

- **Your cart, before you submit it.** The cart you build is held in the app's preferences store on the device. It is only uploaded to our backend at the moment you place the order. If you uninstall the app before placing the order, the cart goes with it.
- **App preferences.** Theme choice, last-used location identifier, and similar short-lived bits — all kept in the device's preferences store.

---

## What we store on our servers

When you place an order, the records described under "Information you give us" are saved to your account on **Supabase**, our backend host.

- Each row is tagged with your account ID. Database row-level security rules enforce that only your signed-in session can read or change your own orders. Other customers cannot see your orders, and you cannot see theirs.
- Restaurant staff (manager, supervisor, cashier roles) can see your orders for operational reasons — preparing the food, taking payment, and following up if something goes wrong. They cannot see your stored Google profile information beyond the name attached to the order.
- Connections to Supabase use HTTPS (encrypted in transit). Data at rest in Supabase is encrypted by their infrastructure.
- We do **not** use end-to-end encryption. That means: in principle, our backend administrators have the technical ability to read data stored in your account. We do not access individual customers' records except when investigating a support request you've raised, debugging a reported bug, or complying with a lawful request.

---

## Payments: how it actually works

We never see your card or bank details. Here's the flow for a paid order:

1. You place an order in the app and choose **GCash** as the payment method.
2. The app shows a GCash QR code provided by the restaurant.
3. You scan the QR in **your own GCash app**, enter the amount, and send the payment. This step happens entirely between you and GCash — our app never sees your GCash PIN, balance, or any other account detail.
4. GCash shows you a reference number for the transaction.
5. You return to the ASA BBQ app and type the reference number into the order.
6. The reference is stored on the order so our staff can confirm the payment was received.

If you'd rather pay in cash at the counter, simply pick **Cash** at checkout. No GCash data is involved at all in that case.

---

## Ads

The home screen of the app shows a single banner advert supplied by **Google AdMob**.

- AdMob and Google's User Messaging Platform (UMP) collect data per Google's own privacy policies. This typically includes your advertising identifier and similar signals. See [Google's privacy policy](https://policies.google.com/privacy) and [how Google uses information from sites or apps that use Google services](https://policies.google.com/technologies/partner-sites).
- If you are in the European Economic Area, the United Kingdom, or any region where Google's UMP determines that consent is required, the app shows a consent form provided by Google before any personalised ad is requested.
- You can opt out of personalised ads at the operating-system level. On Android: **Settings → Privacy → Ads → Delete advertising ID** (or **Opt out of Ads Personalisation** on older devices).

---

## Third-party services we use

| Service | What we use it for | Their policy |
| --- | --- | --- |
| Supabase | Account auth, database, file storage | <https://supabase.com/privacy> |
| Google Sign-In | Letting you sign in at checkout | <https://policies.google.com/privacy> |
| Google AdMob + UMP | The home-screen banner; consent flow | <https://policies.google.com/technologies/ads> |
| GCash (by Mynt) | The customer-side payment app you use to pay | <https://www.gcash.com/privacy-policy/> |

We do not currently use any third-party analytics, crash-reporting, attribution, or tracking service. If we add one, we will list it here and call it out in the app.

---

## Your rights and choices

You can:

- **Sign out.** From the app menu, choose Sign out. Your session ends; your stored orders stay on the account.
- **Stop using the app without deleting anything.** Just uninstall it. The cart on the device is removed; your order history on our backend is not.
- **Delete your account and order history.** Email **support@bluenex.org** from the address tied to your Google sign-in. We'll confirm and then remove your account and the orders linked to it. The full step-by-step lives at our [account-deletion page](./delete-account/).
- **Reset the ads consent form** (if it applies in your region). On Android: clear the app's storage or reinstall — the consent form will be shown again on next launch.

We do not ask you to verify your identity beyond using the same email you signed in with. If you can't sign in (for example, you've lost access to your Google account), write to **support@bluenex.org** with enough detail to confirm the orders are yours, and we'll help.

---

## Children

The app is not directed at children under 13, or under the equivalent minimum age in your country. We do not knowingly collect data from children. If you believe a child has placed an order through the app, contact us and we will remove the records.

---

## Security: what we do, and what we don't claim

We take reasonable steps to protect your data:

- All connections to our backend use HTTPS (encrypted in transit).
- Data at rest in Supabase is encrypted by their infrastructure.
- Database row-level security ensures other customers cannot read or modify your orders.
- We never receive your card, bank, or GCash credentials, so we cannot leak them.

We do **not** claim:

- End-to-end encryption. Our administrators have the technical ability to read order data in your account; we choose not to, except for the support, debugging, and lawful-request reasons listed earlier.
- Perfect security. No system is unbreakable. If we ever discover a breach affecting your data, we will notify affected customers at the email on file as quickly as we can establish what happened.

---

## International users and where data lives

The app is available globally, but it only really makes sense if you can visit the restaurant in Bogo City, Cebu. Wherever you are, your account data is stored on Supabase's managed infrastructure in a Southeast Asia region. Sending your data to that region is a necessary part of using the app, and by signing up you agree to that transfer.

We do not currently make formal claims about compliance with any specific privacy regulation outside the Philippines (such as the EU's GDPR or California's CCPA / CPRA). The rights and choices described above are available to all users regardless of location.

---

## Changes to this policy

When we update this policy, we will:

- Change the "Last updated" date at the top.
- For material changes, surface a notice in the app the next time you open it.

If you continue to use the app after a change, you accept the updated policy. If you don't agree to a change, ask us to delete your account.

---

## Who we are, and how to reach us

The ASA BBQ customer app is built and operated by the ASA BBQ restaurant team in **Bogo City, Cebu, Philippines**.

Email: **support@bluenex.org**

We answer privacy questions at the same address.
