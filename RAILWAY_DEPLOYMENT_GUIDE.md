# TaskManager Frontend - Railway Deployment Guide

## Deploy Frontend on Railway

### **Step 1: Go to Railway**

1. Go to [railway.app](https://railway.app)
2. Login with GitHub
3. Create new project or use existing

### **Step 2: Create New Service**

1. Click **"New Service"** button
2. Select **"Deploy from GitHub"**
3. Choose repository: `piyushchauhanpiy/frontedntaskmanager`

### **Step 3: Configure Frontend**

#### **Basic Settings:**

- **Name**: `taskmanager-frontend`
- **Root Directory**: `/` (root directory)
- **Branch**: `main`

#### **Build Settings:**

- **Builder**: **"Railpack"** (recommended for React)
- **Build Command**: `npm run build`
- **Start Command**: `npm start`

### **Step 4: Add Environment Variables**

#### **Add these variables in Variables Section:**

**Variable 1:**

```
Name: REACT_APP_API_URL
Value: https://taskmanager-backend-5bl5.onrender.com
```

**Variable 2:**

```
Name: REACT_APP_API_TIMEOUT
Value: 30000
```

**Variable 3:**

```
Name: REACT_APP_SUCCESS_MESSAGE_DURATION
Value: 5000
```

**Variable 4:**

```
Name: REACT_APP_ERROR_MESSAGE_DURATION
Value: 5000
```

**Variable 5:**

```
Name: REACT_APP_TASK_SUCCESS_DURATION
Value: 3000
```

### **Step 5: Deploy**

1. Click **"Create Service"**
2. Railway will automatically deploy
3. Wait 2-3 minutes

## Deploy Process

```
Detecting React project...
Installing dependencies...
Building React app...
Starting production server...
Service is live!
```

## After Deployment

### **Frontend URL:**

```
https://taskmanager-frontend-xxxx.railway.app
```

### **Full Application:**

- **Backend**: `https://taskmanager-backend-5bl5.onrender.com`
- **Frontend**: `https://taskmanager-frontend-xxxx.railway.app`

## Important Points

### Do This:

- Use "Railpack" builder in Railway
- Keep root directory as `/`
- Copy backend URL correctly
- Add all environment variables

### Don't Do This:

- Don't use Docker
- Don't forget environment variables
- Don't use wrong backend URL

## Quick Summary

```
1. Railway → New Service → GitHub
2. Repository: piyushchauhanpiy/frontedntaskmanager
3. Root: /
4. Builder: Railpack
5. Build: npm run build
6. Start: npm start
7. Variables: Add 5 variables
8. Deploy!
```

## Success!

**Your TaskManager Frontend will be live on Railway within 10 minutes!**

## Support

If any issues occur:

1. Check Railway logs
2. Verify environment variables
3. Test backend URL
