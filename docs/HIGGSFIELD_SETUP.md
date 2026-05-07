# 🎬 Higgsfield AI — Complete Setup Guide

**Status:** ✅ **LIVE & AUTHENTICATED**

---

## 📊 Account Status

- **Email:** curtisbrooks77@gmail.com
- **Plan:** Plus (required for Soul Character & full CLI)
- **Credits:** 4000
- **CLI Version:** 0.1.32

---

## 🔧 Installation (Already Complete)

```bash
npm install -g @higgsfield/cli
```

**Verify:**
```bash
higgsfield --version
# higgsfield 0.1.32 (66dba2137ff7f9682ef8a9e0f0c90a0e9732e877)
```

---

## 🔐 Authentication (Already Complete)

```bash
higgsfield auth login
# Opens browser → approve at higgsfield.ai/device
```

**Check status:**
```bash
higgsfield account status
# curtisbrooks77@gmail.com — plus plan, 4000 credits
```

---

## 🎨 Pipeline Stages

### Stage 1: Account Setup ✅
- [x] Account created at higgsfield.ai
- [x] Upgraded to Plus plan
- [x] Credits added (4000 available)

### Stage 2: CLI Installation ✅
- [x] Installed `@higgsfield/cli` globally
- [x] Verified version

### Stage 3: Authentication ✅
- [x] Logged in via device flow
- [x] Token saved locally

### Stage 4: Upload Product Images
Upload reference images for product shots:

```bash
higgsfield upload create --file product.jpg
# Returns: upload_id
```

### Stage 5: Product Photoshoot
Generate brand-quality product images:

```bash
# Basic product shot
higgsfield product-photoshoot create \
  --mode lifestyle_scene \
  --prompt "serum bottle on marble counter, morning light, luxury feel" \
  --image <upload_id>

# Floating product
higgsfield product-photoshoot create \
  --mode conceptual_product \
  --prompt "floating product in mid-air, minimalist white background, dramatic shadow" \
  --image <upload_id>

# Close-up with person
higgsfield product-photoshoot create \
  --mode closeup_product_with_person \
  --prompt "hands holding product, partial face, beauty application" \
  --image <upload_id>

# Model try-on
higgsfield product-photoshoot create \
  --mode virtual_model_tryout \
  --prompt "product worn by model, full body, editorial outdoor" \
  --image <upload_id>
```

### Stage 6: Video Generation
Create product videos and motion content:

```bash
# Cinematic product dolly-in
higgsfield generate create cinematic_studio_video \
  --prompt "slow cinematic dolly-in on product, shallow depth of field, luxury feel" \
  --image <upload_id>

# Lifestyle walkthrough
higgsfield generate create kling2_6 \
  --prompt "person walking through luxury apartment, carrying product naturally, natural light" \
  --image <upload_id>

# 360 product spin
higgsfield generate create seedance_2_0 \
  --prompt "product spinning 360 degrees, clean white background, dramatic studio lighting" \
  --image <upload_id>

# UGC unboxing
higgsfield generate create marketing_studio_video \
  --prompt "creator unboxing product, UGC style, authentic reaction, vertical format" \
  --image <upload_id>
```

### Stage 7: Marketing Studio / UGC
Generate UGC-style ads and marketing content:

```bash
# UGC testimonial
higgsfield marketing-studio create \
  --prompt "luxury wellness UGC ad, creator testimonial, 15 seconds, authentic feel" \
  --image <upload_id>

# Before/after transformation
higgsfield marketing-studio create \
  --prompt "before and after skincare transformation, UGC style, soft natural lighting" \
  --image <upload_id>

# Product demo
higgsfield marketing-studio create \
  --prompt "product how-to demo, step by step tutorial, clear and engaging" \
  --image <upload_id>
```

---

## 🧠 Soul Character (Advanced)

Train a consistent virtual character for your brand:

```bash
# Upload 10-20 reference images
higgsfield upload create --file face1.jpg
higgsfield upload create --file face2.jpg
# ... (repeat for all)

# Create Soul ID
higgsfield soul-id create \
  --name "Brand Ambassador" \
  --images <upload_id_1>,<upload_id_2>,<upload_id_3>,...

# Generate with Soul ID
higgsfield generate create soul_cinematic \
  --prompt "cinematic portrait, dramatic side lighting, luxury brand campaign" \
  --soul-id <soul_id>
```

---

## 🎯 Available Models

### Image Models
- **Cinematic Studio 2.5** — High-end product photography
- **FLUX.2** — Fast, high-quality generations
- **GPT Image 2** — OpenAI's image model
- **Higgsfield Soul V2** — Soul Character shots
- **Marketing Studio Image** — UGC-style content
- **Nano Banana Pro** — Fast iterations
- **Kling O1 Image** — Creative control

### Video Models
- **Cinematic Studio 3.0** — Premium video generation
- **Google Veo 3.1** — Google's latest video model
- **Kling v3.0** — High-quality motion
- **Marketing Studio Video** — UGC video ads
- **Seedance 2.0** — Smooth animations
- **Soul Cast** — Character-driven video

---

## 💡 Prompt Tips for Best Results

### Product Photography
- Specify **lighting** (morning light, dramatic, soft, golden hour)
- Include **mood** (luxury, authentic, clean, editorial)
- Add **composition** (close-up, full frame, overhead, side angle)
- Mention **setting** (marble counter, white background, outdoor, studio)

### Video Prompts
- Use **camera movement** (dolly-in, pan, orbit, static)
- Specify **pacing** (slow cinematic, fast-cut, smooth transition)
- Include **depth of field** (shallow DOF, deep focus)
- Add **format** (vertical 9:16 for TikTok/Instagram, horizontal for YouTube)

### UGC / Marketing Studio
- Emphasize **authenticity** (authentic, natural, genuine, real)
- Use **hooks** ("this changed my routine", "you need to try this")
- Specify **duration** (15 seconds, 30 seconds, 60 seconds)
- Mention **vibe** (enthusiastic, calm, energetic, educational)

---

## 🛠️ Workflow Commands

**Check job status:**
```bash
higgsfield generate list
```

**Wait for job completion:**
```bash
higgsfield generate wait <job_id>
```

**Calculate generation cost:**
```bash
higgsfield generate cost <model> --prompt "your prompt here"
```

**List all models:**
```bash
higgsfield model list --image
higgsfield model list --video
```

---

## 🔗 Key Resources

- **Dashboard:** https://higgsfield.ai/dashboard
- **Documentation:** https://docs.higgsfield.ai
- **Device Auth:** https://higgsfield.ai/device
- **API Docs:** https://api.higgsfield.ai/docs

---

## ⚠️ Known Issues

| Issue | Workaround |
|-------|------------|
| Browser doesn't open during `auth login` | Manually visit the printed URL |
| Upload fails with large files | Compress or resize before upload |
| Jobs stuck in "processing" | Wait 2-5 min, check with `generate list` |
| Credits not updating | Refresh with `account status` |

---

## 🚀 Quick Start Workflow

```bash
# 1. Upload product image
higgsfield upload create --file product.jpg
# Note the upload_id

# 2. Generate product shot
higgsfield product-photoshoot create \
  --mode lifestyle_scene \
  --prompt "luxury serum on marble, morning light" \
  --image <upload_id>

# 3. Check job status
higgsfield generate list

# 4. Wait for completion
higgsfield generate wait <job_id>

# 5. Download from dashboard or via CLI
```

---

**You're now a Higgsfield Editor!** 🎬🔥

Run generations, create UGC content, train Soul Characters, and deliver high-end brand assets.
