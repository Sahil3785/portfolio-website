# Deployment Guide for Vercel

## Prerequisites
- GitHub account
- Vercel account (sign up at https://vercel.com)

## Steps to Deploy

### Option 1: Deploy via Vercel Dashboard (Recommended)

1. **Push your code to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Portfolio website"
   git branch -M main
   git remote add origin <your-github-repo-url>
   git push -u origin main
   ```

2. **Import Project to Vercel**
   - Go to https://vercel.com/dashboard
   - Click "Add New Project"
   - Import your GitHub repository
   - Vercel will auto-detect Vite settings

3. **Configure Build Settings**
   - Framework Preset: Vite
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`

4. **Deploy**
   - Click "Deploy"
   - Wait for build to complete
   - Your site will be live!

### Option 2: Deploy via Vercel CLI

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy**
   ```bash
   cd portfolio-website-main
   vercel
   ```

4. **For Production Deployment**
   ```bash
   vercel --prod
   ```

## Important Notes

### Before Deploying:
1. **Update Resume/CV**: Place your resume PDF at `/public/Images/Sahil-Resume.pdf`
2. **Update Profile Image**: Ensure `/public/Images/profileLogo.jpg` is your profile picture
3. **Update Project Images**: Replace project images in `/public/Images/` with your actual project screenshots
4. **Update Social Links**: 
   - Add your GitHub URL in Contact.tsx and Footer.tsx
   - Update LinkedIn URL if different

### Environment Variables (if needed):
If you add any API keys or environment variables later, add them in Vercel Dashboard:
- Go to Project Settings → Environment Variables

### Custom Domain:
1. Go to Project Settings → Domains
2. Add your custom domain
3. Follow DNS configuration instructions

## Post-Deployment Checklist

- [ ] Test all navigation links
- [ ] Verify contact form (if you add backend)
- [ ] Check all social media links
- [ ] Test resume download
- [ ] Verify mobile responsiveness
- [ ] Check SEO meta tags
- [ ] Test all project links

## Troubleshooting

### Build Fails:
- Check Node.js version (project requires Node 18.x, but Node 22.x should work)
- Ensure all dependencies are in package.json
- Check for TypeScript errors

### 404 Errors:
- The vercel.json file handles routing
- Ensure all routes are properly configured

### Images Not Loading:
- Check image paths (should start with `/Images/`)
- Ensure images are in `/public/Images/` directory

## Support

For issues, check:
- Vercel Documentation: https://vercel.com/docs
- Vite Documentation: https://vitejs.dev
