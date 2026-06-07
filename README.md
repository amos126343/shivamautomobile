# M Shoppee Website

Professional Next.js website for **M Shoppee**, a Mahindra genuine spare parts shop and garage service center.

## Features

- Next.js App Router with Tailwind CSS
- Responsive premium automobile UI
- Spare parts catalogue with search and category filter
- Part availability enquiry form with optional photo upload
- Garage service booking form
- Supabase database, auth, and storage integration
- Protected admin dashboard for enquiries, inventory, and service bookings
- WhatsApp reply and confirmation links
- SEO metadata, reusable components, loading states, success and error messages

## Pages

- Home
- About
- Spare Parts
- Check Part Availability
- Garage Services
- Book Service
- Gallery
- Reviews
- Contact
- Admin Login and Dashboard

## Setup

1. Install dependencies:

```bash
npm install
```

2. Create `.env.local`:

```bash
cp .env.example .env.local
```

3. Add your Supabase values:

```env
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
SUPABASE_SERVICE_ROLE_KEY=your-service-role-key
NEXT_PUBLIC_WHATSAPP_NUMBER=919999999999
```

4. In Supabase SQL Editor, run:

```text
supabase/schema.sql
supabase/seed.sql
```

5. Create an admin user in Supabase Auth, then log in at:

```text
/admin/login
```

6. Start development:

```bash
npm run dev
```

Open `http://localhost:3000`.

## Supabase Notes

- `part_enquiries` stores customer parts requests.
- `service_bookings` stores garage bookings.
- `inventory_parts` powers the spare parts catalogue.
- `gallery_images` and `reviews` power public display sections.
- `admin_profiles` can be used to store admin profile data.
- Storage buckets `part-photos` and `product-images` are created by the schema.

The app uses the service role key only in server actions and server components. Do not expose `SUPABASE_SERVICE_ROLE_KEY` in client-side code.

## Customize Business Details

Edit `lib/data.ts` to update:

- Address
- Phone and WhatsApp number
- Email
- Opening hours
- Default gallery images
- Default reviews
- Sample parts and service list
"# shivamautomobile" 
"# shivamautomobile" 
