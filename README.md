UFC Roboflow Stat Counter

A Python + OpenCV video analysis tool that uses a Roboflow Workflow (via `inference`) to classify UFC fight positions frame-by-frame (e.g., standing/clinch vs ground) and compute **cumulative time spent in each state**. The script overlays live timers and frame count on the video preview, prints per-frame predictions/confidence to the console, and can export an annotated MP4.

What it does
- Reads a fight video (`.mp4`)
- Runs Roboflow Workflow inference on frames (up to `max_fps`)
- Detects whether the current frame contains:
  - **Standing / clinch**
  - **Ground**
- Updates running timers for each state
- Overlays timers onto the frame using OpenCV
- Optional: writes an output video with overlays

Demo output
- Live preview window: `UFC Fight Analysis`
- Console logs per frame: prediction classes + confidence + time breakdown
- Output file: `output_fight_with_timers.mp4` (optional, if enabled)

---
Setup

Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate