# CementFlow - Cement Distribution Management System

## Overview
CementFlow is a professional desktop-first web application for managing cement distribution bookings, invoicing, and order tracking. Built with IndexedDB for persistent storage, it works both online and offline with AI-powered smart entry capabilities.

## Login Credentials
- **Username:** `CEMENT`
- **Password:** `419`

## Key Features

### 🔐 Authentication
- Secure login system
- Session-based authentication
- Protected admin features

### 📋 Booking Management
- **Create Bookings:** Manual form entry or AI-powered smart entry
- **Edit Bookings:** Full editing capability for existing orders with change tracking
- **Quick Status Updates:** One-click buttons to progress orders through workflow
- **Activity Logging:** Complete audit trail of all booking changes
- **Payment Tracking:** Separate payment status (Unpaid/Partial/Paid)
- **Delivery Timestamps:** Automatic tracking of delivery confirmation times

### 🤖 AI Smart Entry
- Natural language booking input powered by GPT-5.1
- Automatically extracts customer details, product, quantity, and dates
- Fallback to basic text parsing when offline

### 📊 Dashboard
- Real-time statistics:
  - Total Bookings
  - Total Revenue (GH₵)
  - Pending Orders
  - Delivered Orders
- Recent bookings table with quick actions

### 🔍 Advanced Filtering
- Filter by status (All/Pending/Confirmed/Delivered)
- Customer search by name or phone
- Real-time search results

### 📦 Product Management
- Add/delete cement products
- Set custom pricing per bag
- Default products: Dangote, GHACEM, Diamond Cement

### 💼 Manager Accountability
- **Edit Existing Bookings:** Modify customer details, quantities, status, and payment
- **Quick Workflow Actions:**
  - ✓ Confirm button for pending orders
  - ✓ Deliver button for confirmed orders
- **Activity Log:** Tracks every change with:
  - Timestamp
  - Action performed
  - User attribution
  - Before/after values
- **Booking Details View:** Complete history and current status
- **Payment Status Tracking:** Independent from delivery status
- **Delivery Confirmation:** Automatic timestamping when order marked delivered

### 🧾 Invoice Generation
- Professional print-ready invoices
- Company branding
- Itemized billing
- Clean A4 layout

### 📤 Data Export
- Export bookings to Excel (CSV format)
- Export all data from Admin Panel
- Compatible with Microsoft Excel, Google Sheets, LibreOffice

### ⚙️ Admin Panel
- View database statistics
- Export all data
- Reset all data (with confirmation)
- Restore default products

### 🌐 Offline Support
- IndexedDB persistent storage
- Online/offline status indicator
- All core features work offline (except AI Smart Entry)
- Data syncs automatically

## Usage Instructions

### Creating a Booking

#### Method 1: AI Smart Entry (Online Only)
1. Go to "New Booking" page
2. Enter booking details in natural language:
   ```
   Example: John Mensah needs 50 bags of Dangote cement
   delivered to Accra tomorrow, phone 0244123456
   ```
3. Click "Process with AI"
4. Review auto-filled form
5. Submit

#### Method 2: Manual Entry
1. Go to "New Booking" page
2. Fill in customer details
3. Select product and quantity
4. Set delivery date and status
5. Add notes if needed
6. Click "Create Booking"

### Managing Existing Bookings

#### Quick Status Updates
- **Pending Orders:** Click "✓ Confirm" button to mark as confirmed
- **Confirmed Orders:** Click "✓ Deliver" button to mark as delivered
- All status changes are logged in the activity log

#### Editing a Booking
1. Go to "All Bookings" page
2. Click the Edit icon (pencil) on any booking
3. Modify any fields:
   - Customer name and phone
   - Delivery address
   - Quantity (amount auto-recalculates)
   - Status (pending/confirmed/delivered)
   - Payment status (unpaid/partial/paid)
   - Notes
4. Click "Save Changes"
5. Changes are logged with timestamp

#### Viewing Booking Details
1. Click the Info icon (i) on any booking
2. View complete booking information:
   - Customer details
   - Product and quantity
   - Status and payment status
   - Delivery timestamp (if delivered)
   - Complete activity log with all changes
3. Click "Edit Booking" to make changes directly from details view

### Viewing Bookings
1. Go to "All Bookings" or check Dashboard
2. Use filter chips to view by status
3. Search by customer name or phone
4. Click actions:
   - **Info icon:** View complete details and activity log
   - **Edit icon:** Modify booking
   - **Eye icon:** Generate invoice
   - **Trash icon:** Delete booking

### Exporting Data
1. **Single Export:** Click "Export to Excel" on All Bookings page
2. **Full Export:** Go to Admin Panel → "Export All Data"
3. Opens download dialog for CSV file
4. Compatible with Excel, Google Sheets, LibreOffice

### Managing Products
1. Go to "Products" page
2. View current product catalog
3. Click "Add Product" to add new cement type
4. Set name and price per bag
5. Delete products as needed (with confirmation)

### Admin Functions
1. Go to "Admin Panel" page
2. View database statistics
3. Export complete data backup
4. Reset all data (requires confirmation)

## Activity Log Details

Every booking maintains a complete activity log tracking:
- **Booking Creation:** Initial timestamp and details
- **Status Changes:** From → To status with timestamp
- **Edits:** What was changed and when
- **User Attribution:** Who made the change (Manager)
- **Delivery Confirmation:** Automatic timestamp when delivered

Example Activity Log:
```
2025-01-15 10:30:45 AM
Booking created
By: Manager

2025-01-15 2:15:20 PM
Status changed from pending to confirmed
By: Manager

2025-01-16 9:45:00 AM
Booking edited
Changes: Status: confirmed → delivered, Amount: GH₵4250.00 → GH₵4250.00
By: Manager
```

## Data Storage

### IndexedDB (Persistent Browser Storage)
- All bookings and products stored in browser's IndexedDB
- Data persists across sessions and page refreshes
- Survives browser restarts
- Located in browser's local storage (not cloud)

### Data Retention
- Data remains until manually reset via Admin Panel
- Not affected by page refresh or navigation
- Survives browser closure
- Only cleared by:
  1. Admin reset function
  2. Manual browser data clearing
  3. Browser storage quota exceeded (rare)

## Technical Details

### Technology Stack
- Pure HTML, CSS, JavaScript (no build required)
- IndexedDB for persistent storage
- Poe Embed API for AI features
- IBM Plex Sans font family
- Responsive design (desktop-first)

### Browser Compatibility
- Chrome 87+
- Firefox 78+
- Safari 14+
- Edge 87+
- Requires IndexedDB support

### Online vs Offline Features

#### Works Offline:
- Create/edit/delete bookings
- View all bookings and invoices
- Export data
- Manage products
- All core functionality

#### Requires Online:
- AI Smart Entry feature
- Status indicator shows current connection state

## Color Scheme
- Primary: Orange (#ff6600)
- Background: White with light gray accents
- Professional business aesthetic
- Print-optimized for invoices

## Security Notes
- Login credentials hardcoded (demo application)
- Data stored locally in browser
- No server synchronization
- No cloud backup
- Export data regularly for backup

## Tips for Best Use
1. **Regular Exports:** Export data weekly for backup
2. **Activity Review:** Check booking details to audit changes
3. **Quick Actions:** Use ✓ Confirm and ✓ Deliver buttons for faster workflow
4. **Payment Tracking:** Update payment status independently from delivery
5. **Search Function:** Use customer search to quickly find orders
6. **Print Invoices:** Use browser print (Ctrl+P / Cmd+P) when invoice modal is open
7. **Offline Mode:** All core features work offline except AI Smart Entry

## Troubleshooting

### Login Issues
- Ensure username is exactly: `CEMENT` (all caps)
- Ensure password is exactly: `419`
- Clear browser cache if persistent issues

### Data Not Saving
- Check browser storage settings
- Ensure IndexedDB is not disabled
- Check browser console for errors
- Try different browser

### AI Smart Entry Not Working
- Check internet connection
- Status indicator should show "Online"
- Falls back to basic parsing if unavailable
- Can always use manual entry

### Export Not Working
- Check browser download settings
- Allow pop-ups for this site
- Try different browser

## Version History

### v1.3 - Manager Accountability Update
- ✅ Edit existing bookings with full change tracking
- ✅ Quick status update buttons (✓ Confirm, ✓ Deliver)
- ✅ Activity log for complete audit trail
- ✅ Payment status tracking (unpaid/partial/paid)
- ✅ Delivery confirmation timestamps
- ✅ Booking details modal with activity history
- ✅ Enhanced table with 4 actions per booking

### v1.2 - Database & Authentication Update
- ✅ IndexedDB persistent storage
- ✅ Login authentication system
- ✅ Admin panel with reset/export
- ✅ Excel/CSV export functionality
- ✅ White and orange theme

### v1.1 - Initial Release
- ✅ AI Smart Entry
- ✅ Booking management
- ✅ Invoice generation
- ✅ Product catalog
- ✅ Dashboard statistics

## Support
For issues or questions, check browser console for error messages.

---

**CementFlow** - Professional Cement Distribution Management
Built with Claude Code for Poe Canvas Apps
