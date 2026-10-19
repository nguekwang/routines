# Hair Salon

Runs every Saturday morning. What to do depends on the date:
- Date is the 1st–7th (first Saturday of the month) → run [A: Haircut day]
- Date is the 15th–21st (third Saturday of the month) → run [B: Book next month's haircut]
- Any other date → do nothing and end immediately (no notification needed)

## Common: purpose reminder — always show this at the very start of every run
Why I cut my hair:
1. To shorten the time spent on bathing, drying and styling (lower the cost of getting ready in the morning)
2. To look clean and well-groomed, raising my "humanity" and building influence

→ An investment in standing in front of people with confidence.

## Background
The user (USER_NAME) gets a haircut about every 4 weeks. The haircut is always on the first Saturday of each month, and it is booked on the third Saturday of the previous month.

## A: Haircut day (first Saturday)
1. Check Google Calendar (connector) for today's "散髪" event and its booking details (salon name, time, location, booking URL/phone number), and report them briefly together with the purpose reminder.
2. If there is no haircut event today, or the booking is not confirmed (title contains 【要予約】), find salons that can be booked right away (around HOME_AREA, with online booking URL and phone number) and, if possible, book an open slot for today (same procedure as step 3 of [B]). Reflect the result in the calendar.
3. Add one short tip on how to order the cut (e.g., ask for a style that dries quickly and is easy to set).

## B: Book next month's haircut (third Saturday)
1. The booking date is the first Saturday of the following month (the month after the one this third Saturday falls in). Calculate the date precisely from the current date.
2. Search around HOME_AREA for inexpensive, well-reviewed hair salons/barbers (men's cuts, good at low-maintenance styles that are quick to set). Also check the shop in the Google Maps link the user uses as a reference, https://maps.app.goo.gl/1y2xdRJy9Q7XZ1N26, and include it in the comparison. Give 2–3 candidates with price, rating, opening hours and booking method (online booking URL/phone number).
3. Actually book a morning slot on the booking date (first Saturday of next month) at the top candidate. If online booking is possible via browser, confirm the booking with the name BOOKING_NAME and email BOOKING_EMAIL. The user cannot be asked for confirmation during this run, so do not stop to wait for confirmation. However, if payment information (card number, etc.) is required, do not book; move on to the fallback in steps 4–5. If the first candidate is full, try the second candidate and onward.
4. Whether or not the booking succeeded, always add an event "散髪(salon name)" on the first Saturday of next month in Google Calendar (connector). If the booking is confirmed, include 「予約済み」 in the title; if not, include 「【要予約】」. (Keep these calendar title keywords in Japanese exactly as written, since existing events are matched by them.) In the description, put the two purposes above and the salon's booking URL/phone number. Time: the booked slot (if unconfirmed, 10:00 AM, 1 hour). Set reminders 15 minutes before and the day before. If a haircut event already exists on that date, do not create a duplicate.
5. If the booking could not be made, add a Todoist task "Book a haircut (salon name / booking URL)" due two days before the booking date (if the Todoist connector is available).

## Finally
Summarize the result briefly: the purpose reminder; (A) today's booking details / (B) candidate salons, booking date and time, whether the booking was confirmed, whether the calendar event was added; and the one next action the user should take (only if the booking is unconfirmed).

Write all messages to the user in English. Japanese salon names, addresses and other proper nouns may stay as they are.
