Build and deploy my **MediaFlow Premium** video downloader web application.

Use my existing MediaFlow project as the starting point. Preserve its functionality while upgrading the interface and adapting the architecture for Vercel.

### Design
- Premium, colorful dark theme.
- Purple, blue, pink and cyan gradients.
- Glassmorphism cards, subtle glow effects and smooth animations.
- Responsive desktop and mobile layout.
- Professional dashboard with a polished sidebar and navigation.

### Features
1. Support YouTube, Facebook, TikTok, Kick and Twitch.
2. Accept multiple video URLs, up to 10 at once.
3. MP4 video and MP3 audio output.
4. Video quality selection.
5. Download queue with progress indicators.
6. Download history.
7. Clear error messages and loading states.
8. Copy URL, remove jobs and refresh history.
9. Mobile-friendly interface.

### Deployment architecture
- Deploy the frontend using Vercel.
- Use Next.js with TypeScript and Tailwind CSS.
- Build API routes for submitting jobs and retrieving job status.
- Do not attempt long-running video processing inside Vercel serverless functions.
- Keep yt-dlp and FFmpeg processing in a separate background worker deployed on a suitable service such as Railway or Render.
- Use Redis or another persistent queue for jobs and a persistent database for download history.
- Store secrets in environment variables, never in frontend code.
- Configure production API URLs and CORS correctly.

### Important
- Do not create a fake downloader or simulate successful downloads.
- Connect the UI to real backend APIs.
- Clearly display unsupported URLs and processing errors.
- Only process media users own or have permission to download.
- Do not bypass DRM, private content restrictions or access controls.
- Include a README with complete deployment instructions.
- Provide a `.env.example` file.
- Make sure the project builds successfully before finishing.

Deliver a complete, working, production-ready project with a premium visual design.