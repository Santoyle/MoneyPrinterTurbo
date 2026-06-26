# Manual Publishing Checklist

Use this checklist for every video before and after manual publication.
Complete each step in order. Do not publish until all pre-publish steps are checked.

---

## Pre-publish review

### 1. Video file
- [ ] Locate `storage/tasks/{task_id}/final-1.mp4` on local machine
- [ ] File exists and is not 0 bytes
- [ ] Play full video from start to finish without skipping

### 2. Audio
- [ ] Narration is audible throughout the entire video
- [ ] No silent gaps longer than ~1 second
- [ ] Voice is clear, correct language, natural pacing
- [ ] Background music is present and not overwhelming narration

### 3. Subtitles
- [ ] Subtitles are visible (white text, black background)
- [ ] Text is readable at typical phone viewing size
- [ ] Subtitles are in the correct language
- [ ] Subtitles sync correctly with narration (no obvious lag)

### 4. Visual content
- [ ] Footage is relevant to the topic (not completely random or jarring)
- [ ] No frozen frames, black frames, or visual glitches
- [ ] 9:16 portrait orientation confirmed
- [ ] Resolution looks sharp (1080×1920)

### 5. Script / content quality
- [ ] Hook lands in the first 2–3 seconds
- [ ] No factual errors or misleading claims
- [ ] Language tone matches the intended audience
- [ ] Actionable close is clear and specific
- [ ] No banned clichés or generic phrases from the blocklist

---

## Publishing preparation

### 6. Platform selection
- [ ] Choose platform for this video: TikTok / Instagram Reels / LinkedIn / YouTube Shorts
- [ ] Confirm the platform fits the topic tone (contrarian → TikTok/IG; reflective → LinkedIn)

### 7. Title / caption
- [ ] Copy the title from the publish pack (`spanish_ai_productivity_publish_pack_v1.csv`)
- [ ] Copy the caption from the publish pack
- [ ] Review caption for length: TikTok/IG ~150 chars max visible; LinkedIn can be longer
- [ ] Verify no sensitive information in caption

### 8. Hashtags
- [ ] Copy hashtags from publish pack (5–8 hashtags max)
- [ ] Confirm hashtags are in Spanish for Spanish-language content
- [ ] Do not add more than 3 extra hashtags beyond the pack list

### 9. Thumbnail / cover frame
- [ ] If the platform allows a cover frame, choose a frame with clear subtitle text visible
- [ ] Suggested frame from publish pack: use timestamp noted in `thumbnail_suggestion` column
- [ ] Take a screenshot of that frame from the video if needed

---

## Publication

### 10. Upload (manual only)
- [ ] Open the platform app or website manually
- [ ] Upload `final-1.mp4` directly — do NOT use any automated upload script
- [ ] Paste the title
- [ ] Paste the caption
- [ ] Paste the hashtags
- [ ] Set the cover frame if applicable
- [ ] Set language / audience filters if the platform offers them
- [ ] Review the preview before posting
- [ ] Confirm `upload_post_enabled = false` and `auto_upload = false` remain in config.toml

### 11. Publish
- [ ] Tap / click publish
- [ ] Confirm the post appears in the profile / feed
- [ ] Copy the post URL

---

## Post-publish tracking

### 12. Record in tracker
- [ ] Open `content/publishing/publishing_tracker_v1.csv`
- [ ] Find the row for this video (match by `id` or `topic`)
- [ ] Update `status` → `published`
- [ ] Fill in `publish_date` (YYYY-MM-DD)
- [ ] Fill in `url` (direct link to the post)
- [ ] Leave metrics columns blank — fill after 24h and 7d

### 13. 24-hour check
- [ ] Return 24 hours after publication
- [ ] Record `views_24h` from platform analytics
- [ ] Note anything unusual in `notes` column

### 14. 7-day check
- [ ] Return 7 days after publication
- [ ] Record `views_7d`, `likes_7d`, `comments_7d`, `saves_7d`
- [ ] Update `notes` with any insights (strong hook, weak retention, viral spike, etc.)
- [ ] Decide: does this topic or format deserve a follow-up video?

---

## Notes

- Never activate `upload_post_enabled` or `auto_upload` in config.toml
- Never run any script that touches publishing APIs
- All metrics are recorded manually — no platform API calls
- If a video underperforms (<500 views in 7 days), note the likely cause before creating similar topics
- If a video overperforms (>5k views in 7 days), note the hook, topic type, and format for replication
