# Environment Variables Setup for Vercel

After deployment, you need to add these environment variables in your Vercel dashboard:

## Required Variables (Add these in Vercel Dashboard > Settings > Environment Variables)

### Core Configuration
```
OPENAI_API_KEY=your_openai_api_key_here
NEXTAUTH_SECRET=your_random_secret_key_here
```

### Search Provider (choose one)
```
TAVILY_API_KEY=your_tavily_api_key_here
```

### Optional Features
```
ENABLE_SAVE_CHAT_HISTORY=true
NEXT_PUBLIC_ENABLE_SHARE=true
```

### Additional AI Providers (optional)
```
ANTHROPIC_API_KEY=your_anthropic_api_key
GOOGLE_GENERATIVE_AI_API_KEY=your_google_api_key
GROQ_API_KEY=your_groq_api_key
```

### Redis for Chat History (optional)
```
UPSTASH_REDIS_REST_URL=your_upstash_redis_url
UPSTASH_REDIS_REST_TOKEN=your_upstash_redis_token
USE_LOCAL_REDIS=false
```

## How to Add Environment Variables in Vercel:

1. Go to your Vercel dashboard
2. Select your deployed project
3. Go to Settings > Environment Variables
4. Add each variable with name and value
5. Set environment to "Production" (and "Preview" if needed)
6. Click "Save"
7. Redeploy your application

## Generate NEXTAUTH_SECRET:
```bash
openssl rand -base64 32
```

Or use online generator: https://generate-secret.vercel.app/32

## Get API Keys:
- OpenAI: https://platform.openai.com/api-keys
- Tavily: https://app.tavily.com/
- Anthropic: https://console.anthropic.com/
- Google AI: https://makersuite.google.com/app/apikey
- Upstash Redis: https://console.upstash.com/