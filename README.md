# WhatsApp Voice to Notion Ideas (n8n Workflow)

## 🔄 What does this workflow do?

It converts a **voice message received on WhatsApp** into **text** and automatically saves it in a **Notion page**.

---

## 📌 Step-by-step

### 🎧 WhatsApp Trigger
Detects when someone sends a **voice message** via WhatsApp.  
This is the trigger that starts the workflow.

### 🔗 Get Audio URL
Extracts the **URL of the audio file** from the message.  
It doesn’t download the file yet—just gets the link.

### ⬇️ Download Audio
Uses the URL to **download the voice file**.  
Now the file is ready to be processed.

### 🧠 Transcribe with OpenAI
Sends the audio to **OpenAI Whisper** to convert it into text.  
It “listens” to the voice and returns the transcript.

### 📓 Save to Notion
Creates a new **Notion page** with the transcribed text.  
- The page title is the current date  
- The content is saved as a **bulleted list**

---

## ✅ What you need for this to work

1. A **WhatsApp API** account connected to n8n  
2. A **Notion** account with a page or database to save notes  
3. An **OpenAI** account (for audio transcription)  
4. All credentials set up properly inside **n8n**

---

## ☁️ WhatsApp Cloud API Requirements

To use **WhatsApp Cloud API** with n8n, you need:

- A [Meta/Facebook Business Account](https://business.facebook.com)
- A **verified phone number** (not used with WhatsApp already)
- A **WhatsApp App** created in [Facebook Developers](https://developers.facebook.com)
- A **long-lived access token**
- Webhooks set up to receive messages
- Your **Phone Number ID** and **WhatsApp Business Account ID**

---

## 💡 Tips

- Only works with **voice messages**
- Make sure the audio URL is still valid (WhatsApp links expire quickly)
- You can customize the **Notion layout** in the workflow to change the output format