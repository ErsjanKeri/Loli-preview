# Loli Video Generator

> **AI-Generated Educational Videos with Mathematical Animations**

An advanced educational video generation platform powered by multiple AI models including AWS Bedrock and OpenAI that creates stunning mathematical animations using Manim.

## **Featured AI-Generated Videos**

*Experience the power of AI-driven educational content creation. Each video is generated from a simple text prompt using our multi-stage AI pipeline.*

### **Mathematics & Physics**
- **[Pythagorean Theorem Visual Proof](https://drive.google.com/file/d/1W6SSUpsupFJBGsY4lsCiCEpCabvubSdw/view?usp=drive_link)** - Interactive geometric demonstration of the fundamental theorem
- **[Matrix Multiplication Explained](https://drive.google.com/file/d/1OCSYi6uJcVksfRSRJnlTZsLm19P8BNd4/view?usp=drive_link)** - Step-by-step visual breakdown of matrix operations
- **[Vector Addition in 2D Space](https://drive.google.com/file/d/1UPJFFhrDHfXxWxeOr66Xyk6DPvJ-Xrg9/view?usp=drive_link)** - Animated vector mathematics with geometric intuition
- **[Solenoid Magnetic Field Physics](https://drive.google.com/file/d/1PnBSnhaJwRTIKrOl96FKSbC8w75R9JIb/view?usp=drive_link)** - Electromagnetic field visualization and physics principles

### **Machine Learning & AI**
- **[Deep Learning vs Machine Learning](https://drive.google.com/file/d/1O17pIA7vCQOK8MfmUqn2feNcYTeUFQM8/view?usp=drive_link)** - Distinction between AI paradigms with visual examples
- **[Linear Regression from Scratch](https://drive.google.com/file/d/17atRcaWlTKFZX85hACK1QK7js3XSJoE5/view?usp=drive_link)** - Mathematical foundations with animation
- **[Support Vector Machine (SVM)](https://drive.google.com/file/d/1S48kPJqnKGFdZWIPR30PkYUWaxF6YTlH/view?usp=drive_link)** - Decision boundaries and kernel tricks visualization

### **Computer Science & Algorithms**
- **[Binary Search Algorithm](https://drive.google.com/file/d/1XrDg_KE68KC_95kB8jP9wuFSndr7kjZU/view?usp=drive_link)** - Divide-and-conquer strategy with animated array traversal
- **[Perfect Hashing Techniques](https://drive.google.com/file/d/1l12I31p_FQcP2_7spK7bhMIFBPziBeLg/view?usp=drive_link)** - Hash function design and collision resolution
- **[Maximum Flow Min-Cut Problem](https://drive.google.com/file/d/1X0Q0bpgjpBg79C5ILcViTg3lUG_zxQS6/view?usp=drive_link)** - Graph theory and network flow optimization
- **[Horizontal vs Vertical Scaling](https://drive.google.com/file/d/15gvas3UmJ1h56xzf0Zds7x54OtvYtB6G/view?usp=drive_link)** - Software engineering architecture patterns

### **Chemistry**
- **[Geometric Isomers in Organic Chemistry](https://drive.google.com/file/d/1nAxLbANKIiKcRm-IvrSFWXzwY9riCBsX/view?usp=drive_link)** - 3D molecular structure and stereochemistry

[**View All Videos in Google Drive**](https://drive.google.com/drive/folders/1Kwbone8isI3VavxUGmVjprTHNCfXL_EZ?usp=drive_link)

## API Endpoints

### Configuration

- `GET /api/v1/config` - Get available models and voices

### Video Management

- `POST /api/v1/videos` - Create a new video generation request with model and voice selection
- `GET /api/v1/videos/{video_id}/status` - Check video generation status
- `GET /api/v1/videos/{video_id}/download` - Download completed video 
- `DELETE /api/v1/videos/{video_id}` - Delete video and files
- `GET /api/v1/videos` - List all videos (with optional status filter)

### System Management
- `GET /api/v1/health` - System health check
- `GET /api/v1/stats` - API usage statistics
- `POST /api/v1/cleanup` - Manually trigger cleanup of old videos

**Create a video with model and voice selection:**
```bash
curl -X POST "http://localhost:8000/api/v1/videos" \
  -H "Content-Type: application/json" \
  -d '{
    "prompt": "Explain Maximum Flow problem",
    "model": "claude-4-sonnet",
    "voice": "Joanna"
  }'
```



