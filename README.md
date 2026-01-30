# Invoice Jasper Reports

Multilingual invoice templates for **iDempiere** using **JasperReports**.

# Features

- ✅ **Multilingual** - Automatic translation via iDempiere `AD_Message`
- ✅ **Generic fonts** - `SansSerif`/`Helvetica` (no font compatibility issues)
- ✅ **Subreport optimized** - Clean separation of header/lines/tax

## 🌐 How Translation Works

Reports use **iDempiere's message system** (`org.compiere.util.Msg.translate`): Key → AD_Message_Trl → AD_Message → Default Text

**Translation Priority:**
1. **Exact key** in `Element`
2. **Translation** in `AD_Message` (e.g., `"Phone"`)
3. **Falls back to hardcoded default** (e.g., `"Phone Number"`)

## Customize Labels (No Code Changes!)

**To change any label or add translations:**

1. **Login to iDempiere** → **System Administrator** role
2. Open the **Message** window
3. **Search** by `Value` (e.g., `Phone`, `ContactName`, `EMail`)
4. **Edit** `MsgText` or **add Translation** for new languages
5. **Alternatively Add** the message translation at the tenant level



**Common Message Keys used:**

- Phone → "Phone Number"
- ContactName → "Contact Person"
- EMail → "Email"
- BX_ClientNo → "Client Number"
- BX_NotCompleted → Draft Document - Not yet completed!
- BX_UST → Your USt-ID
- POReference → "Order Reference"

## Deployment

1. **Copy `*.jrxml` files and `styles.jrtx`** to iDempiere report folder
2. Create the **Report & Process** record pointing to the file `C_Invoice_Document.jrxml`
3. Configure the logo on Org Info or Client Info
4. **Test** with different languages
