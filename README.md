<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PostureGuard Pro Store - Setup Guide</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
</head>
<body class="bg-gray-50 text-gray-800">
    <div class="max-w-4xl mx-auto py-8 px-4">
        <div class="bg-white rounded-lg shadow-lg p-8">
            <div class="text-center mb-8">
                <h1 class="text-4xl font-bold text-blue-600 mb-2">
                    <i class="fas fa-store mr-3"></i>PostureGuard Pro Store
                </h1>
                <p class="text-lg text-gray-600">Complete E-commerce Store with Stripe Integration</p>
                <div class="mt-4 flex justify-center space-x-4">
                    <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm">
                        <i class="fab fa-github mr-1"></i>GitHub Ready
                    </span>
                    <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm">
                        <i class="fas fa-cloud mr-1"></i>Netlify Compatible
                    </span>
                    <span class="bg-purple-100 text-purple-800 px-3 py-1 rounded-full text-sm">
                        <i class="fab fa-stripe mr-1"></i>Stripe Integrated
                    </span>
                </div>
            </div>

            <div class="space-y-8">
                <!-- Overview -->
                <section class="border-l-4 border-blue-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-info-circle mr-2 text-blue-500"></i>Overview
                    </h2>
                    <p class="text-gray-700 mb-4">
                        A professional e-commerce store for PostureGuard Pro smart posture corrector with complete Stripe payment integration, 
                        admin dashboard, and automated order management system.
                    </p>
                    <div class="bg-blue-50 p-4 rounded-lg">
                        <h3 class="font-semibold mb-2">Features:</h3>
                        <ul class="list-disc list-inside space-y-1 text-sm">
                            <li>Responsive design with product gallery</li>
                            <li>Secure Stripe payment processing</li>
                            <li>Admin dashboard for order management</li>
                            <li>Customer contact form</li>
                            <li>Automated email notifications</li>
                            <li>Mobile-optimized checkout</li>
                        </ul>
                    </div>
                </section>

                <!-- File Structure -->
                <section class="border-l-4 border-green-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-folder-tree mr-2 text-green-500"></i>File Structure
                    </h2>
                    <div class="bg-gray-100 p-4 rounded-lg font-mono text-sm">
                        <pre class="text-gray-800">
postureguard-pro-store/
├── index.html                  # Main store page
├── package.json               # Dependencies & scripts
├── netlify.toml              # Netlify configuration
├── .env.example              # Environment variables template
├── README.md                 # This documentation
├── netlify/
│   └── functions/
│       ├── create-payment-intent.js  # Stripe payment processing
│       ├── webhook.js                # Stripe webhooks
│       └── send-email.js             # Email notifications
└── .gitignore                # Git ignore file
                        </pre>
                    </div>
                </section>

                <!-- Quick Setup -->
                <section class="border-l-4 border-purple-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-rocket mr-2 text-purple-500"></i>Quick Setup
                    </h2>
                    <div class="space-y-4">
                        <div class="bg-purple-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-2 flex items-center">
                                <span class="bg-purple-500 text-white rounded-full w-6 h-6 flex items-center justify-center text-sm mr-2">1</span>
                                Clone Repository
                            </h3>
                            <div class="bg-gray-800 text-green-400 p-3 rounded font-mono text-sm">
                                git clone https://github.com/yourusername/postureguard-pro-store.git<br>
                                cd postureguard-pro-store
                            </div>
                        </div>

                        <div class="bg-purple-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-2 flex items-center">
                                <span class="bg-purple-500 text-white rounded-full w-6 h-6 flex items-center justify-center text-sm mr-2">2</span>
                                Install Dependencies
                            </h3>
                            <div class="bg-gray-800 text-green-400 p-3 rounded font-mono text-sm">
                                npm install
                            </div>
                        </div>

                        <div class="bg-purple-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-2 flex items-center">
                                <span class="bg-purple-500 text-white rounded-full w-6 h-6 flex items-center justify-center text-sm mr-2">3</span>
                                Configure Environment Variables
                            </h3>
                            <div class="bg-gray-800 text-green-400 p-3 rounded font-mono text-sm">
                                cp .env.example .env<br>
                                # Edit .env with your Stripe keys
                            </div>
                        </div>

                        <div class="bg-purple-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-2 flex items-center">
                                <span class="bg-purple-500 text-white rounded-full w-6 h-6 flex items-center justify-center text-sm mr-2">4</span>
                                Deploy to Netlify
                            </h3>
                            <div class="bg-gray-800 text-green-400 p-3 rounded font-mono text-sm">
                                netlify deploy --prod
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Environment Variables -->
                <section class="border-l-4 border-yellow-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-key mr-2 text-yellow-500"></i>Environment Variables
                    </h2>
                    <p class="mb-4 text-gray-700">Create a <code class="bg-gray-200 px-2 py-1 rounded">.env</code> file in the root directory:</p>
                    <div class="bg-yellow-50 p-4 rounded-lg">
                        <div class="bg-gray-800 text-green-400 p-4 rounded font-mono text-sm">
                            <pre>
# Stripe Configuration
STRIPE_SECRET_KEY=sk_live_your_secret_key_here
STRIPE_PUBLISHABLE_KEY=pk_live_your_publishable_key_here
STRIPE_WEBHOOK_SECRET=whsec_your_webhook_secret_here

# Email Configuration (Optional)
EMAIL_SERVICE_API_KEY=your_email_service_key
ADMIN_EMAIL=admin@postureguardpro.com

# Site Configuration
SITE_URL=https://your-site.netlify.app
                            </pre>
                        </div>
                    </div>
                    <div class="mt-4 bg-red-50 border border-red-200 p-3 rounded-lg">
                        <p class="text-red-800 text-sm">
                            <i class="fas fa-exclamation-triangle mr-2"></i>
                            <strong>Security Warning:</strong> Never commit your .env file to GitHub. It's already included in .gitignore.
                        </p>
                    </div>
                </section>

                <!-- Stripe Setup -->
                <section class="border-l-4 border-indigo-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fab fa-stripe mr-2 text-indigo-500"></i>Stripe Integration Setup
                    </h2>
                    
                    <div class="space-y-4">
                        <div class="bg-indigo-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Step 1: Stripe Account Setup</h3>
                            <ol class="list-decimal list-inside space-y-2 text-sm">
                                <li>Create account at <a href="https://stripe.com" class="text-blue-600 underline">stripe.com</a></li>
                                <li>Complete business verification</li>
                                <li>Go to Developers → API Keys</li>
                                <li>Copy your Publishable and Secret keys</li>
                                <li>Add keys to your Netlify environment variables</li>
                            </ol>
                        </div>

                        <div class="bg-indigo-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Step 2: Webhook Configuration</h3>
                            <ol class="list-decimal list-inside space-y-2 text-sm">
                                <li>In Stripe Dashboard, go to Developers → Webhooks</li>
                                <li>Click "Add endpoint"</li>
                                <li>Endpoint URL: <code>https://your-site.netlify.app/.netlify/functions/webhook</code></li>
                                <li>Select events: <code>payment_intent.succeeded</code></li>
                                <li>Copy the webhook secret to your environment variables</li>
                            </ol>
                        </div>

                        <div class="bg-indigo-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Step 3: Test Mode</h3>
                            <p class="text-sm mb-2">Use these test card numbers:</p>
                            <div class="bg-gray-800 text-green-400 p-3 rounded font-mono text-xs">
                                Success: 4242 4242 4242 4242<br>
                                Decline: 4000 0000 0000 0002<br>
                                3D Secure: 4000 0025 0000 3155
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Netlify Deployment -->
                <section class="border-l-4 border-teal-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-cloud-upload-alt mr-2 text-teal-500"></i>Netlify Deployment
                    </h2>
                    
                    <div class="space-y-4">
                        <div class="bg-teal-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Method 1: GitHub Integration (Recommended)</h3>
                            <ol class="list-decimal list-inside space-y-2 text-sm">
                                <li>Push your code to GitHub repository</li>
                                <li>Connect GitHub repo to Netlify</li>
                                <li>Configure build settings:
                                    <div class="bg-gray-800 text-green-400 p-2 rounded font-mono text-xs mt-2">
                                        Build command: npm run build<br>
                                        Publish directory: (leave blank)
                                    </div>
                                </li>
                                <li>Add environment variables in Netlify dashboard</li>
                                <li>Deploy automatically on push</li>
                            </ol>
                        </div>

                        <div class="bg-teal-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Method 2: Manual Deployment</h3>
                            <div class="bg-gray-800 text-green-400 p-3 rounded font-mono text-sm">
                                npm install -g netlify-cli<br>
                                netlify login<br>
                                netlify init<br>
                                netlify deploy --prod
                            </div>
                        </div>

                        <div class="bg-teal-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Environment Variables in Netlify</h3>
                            <p class="text-sm mb-2">Add in Site Settings → Environment Variables:</p>
                            <ul class="list-disc list-inside space-y-1 text-sm">
                                <li><code>STRIPE_SECRET_KEY</code> - Your Stripe secret key</li>
                                <li><code>STRIPE_PUBLISHABLE_KEY</code> - Your Stripe publishable key</li>
                                <li><code>STRIPE_WEBHOOK_SECRET</code> - Webhook endpoint secret</li>
                            </ul>
                        </div>
                    </div>
                </section>

                <!-- Admin Dashboard -->
                <section class="border-l-4 border-red-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-user-shield mr-2 text-red-500"></i>Admin Dashboard
                    </h2>
                    <div class="bg-red-50 p-4 rounded-lg">
                        <h3 class="font-semibold mb-3">Access & Features</h3>
                        <ul class="list-disc list-inside space-y-2 text-sm">
                            <li><strong>Access:</strong> Click the gear icon (🔧) in the footer</li>
                            <li><strong>Default Password:</strong> <code>admin123</code> (Change this!)</li>
                            <li><strong>Features:</strong> Order management, customer details, tracking updates</li>
                            <li><strong>Security:</strong> Password protection, session management</li>
                        </ul>
                        
                        <div class="mt-4 p-3 bg-yellow-100 border border-yellow-300 rounded">
                            <p class="text-yellow-800 text-sm">
                                <i class="fas fa-warning mr-2"></i>
                                <strong>Important:</strong> Change the default admin password in the code before deploying to production!
                            </p>
                        </div>
                    </div>
                </section>

                <!-- Customization -->
                <section class="border-l-4 border-pink-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-paint-brush mr-2 text-pink-500"></i>Customization
                    </h2>
                    <div class="grid md:grid-cols-2 gap-4">
                        <div class="bg-pink-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-2">Product Information</h3>
                            <ul class="text-sm space-y-1">
                                <li>• Update product images in <code>index.html</code></li>
                                <li>• Modify product description and pricing</li>
                                <li>• Add/remove product features</li>
                                <li>• Update testimonials and reviews</li>
                            </ul>
                        </div>
                        
                        <div class="bg-pink-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-2">Branding</h3>
                            <ul class="text-sm space-y-1">
                                <li>• Replace logo and brand colors</li>
                                <li>• Update contact information</li>
                                <li>• Modify footer and header content</li>
                                <li>• Customize email templates</li>
                            </ul>
                        </div>
                    </div>
                </section>

                <!-- Maintenance -->
                <section class="border-l-4 border-gray-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-tools mr-2 text-gray-500"></i>Maintenance & Monitoring
                    </h2>
                    <div class="space-y-4">
                        <div class="bg-gray-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Regular Tasks</h3>
                            <ul class="list-disc list-inside space-y-2 text-sm">
                                <li>Monitor Stripe dashboard for payments and disputes</li>
                                <li>Check Netlify function logs for errors</li>
                                <li>Update dependencies regularly: <code>npm update</code></li>
                                <li>Backup customer data and order information</li>
                                <li>Monitor site performance and uptime</li>
                            </ul>
                        </div>

                        <div class="bg-gray-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Troubleshooting</h3>
                            <div class="space-y-2 text-sm">
                                <div>
                                    <strong>Payment failures:</strong> Check Stripe logs and webhook configuration
                                </div>
                                <div>
                                    <strong>Function errors:</strong> Review Netlify function logs in dashboard
                                </div>
                                <div>
                                    <strong>Email issues:</strong> Verify email service configuration and API keys
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- Support -->
                <section class="border-l-4 border-blue-500 pl-4">
                    <h2 class="text-2xl font-semibold mb-4 flex items-center">
                        <i class="fas fa-life-ring mr-2 text-blue-500"></i>Support & Resources
                    </h2>
                    <div class="grid md:grid-cols-2 gap-4">
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Documentation</h3>
                            <ul class="space-y-2 text-sm">
                                <li><a href="https://stripe.com/docs" class="text-blue-600 underline">Stripe Documentation</a></li>
                                <li><a href="https://docs.netlify.com" class="text-blue-600 underline">Netlify Documentation</a></li>
                                <li><a href="https://docs.github.com" class="text-blue-600 underline">GitHub Documentation</a></li>
                            </ul>
                        </div>
                        
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <h3 class="font-semibold mb-3">Contact</h3>
                            <ul class="space-y-2 text-sm">
                                <li><i class="fas fa-envelope mr-2"></i>support@postureguardpro.com</li>
                                <li><i class="fas fa-phone mr-2"></i>+1 202 773 7185</li>
                                <li><i class="fas fa-map-marker-alt mr-2"></i>Champlin, MN 55316</li>
                            </ul>
                        </div>
                    </div>
                </section>
            </div>

            <div class="mt-12 text-center p-6 bg-gradient-to-r from-blue-500 to-purple-600 rounded-lg text-white">
                <h2 class="text-2xl font-bold mb-2">Ready to Launch!</h2>
                <p class="mb-4">Your PostureGuard Pro store is configured and ready for deployment.</p>
                <div class="flex justify-center space-x-4 text-sm">
                    <span><i class="fas fa-check mr-1"></i>Secure Payment Processing</span>
                    <span><i class="fas fa-check mr-1"></i>Mobile Optimized</span>
                    <span><i class="fas fa-check mr-1"></i>Admin Dashboard</span>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
    <script id="html_badge_script1">
        window.__genspark_remove_badge_link = "https://www.genspark.ai/api/html_badge/" +
            "remove_badge?token=To%2FBnjzloZ3UfQdcSaYfDlLj8PV8RWu7NFfUUc8UudsCksmSxbrrylIy4Cd95Lj1I1UR2gonTplmajUQRnY3nZ6%2Fvx0Xlf5AHpgCLHCZmc6mPTiZVnVMYKHsCdCAPniw76HCIoAEPwvlztmNP9vjmxErnt%2BgM5Ny9ISxoTjx%2Fi7DQSt4i5yFXVCY%2BZP8QOqWfpWqOofqYG6nGzeKtTHHDeH0wotDttqicbn3KrV55knYzMFtGUpmdYV7Au7s7OeHG4AP7QFkqJzMYvKDGxm6uyyXHxyq6ipv6DEMzOquBoxSqdHqxOso2gTs7eByEai04PccGPuyBFDBWyfmlnEngJLBatgXeR7xhFkLqw%2FcpbhEt514sTGWinBrkjkErBua5p2%2F30l8jyBmYdFfnMBFTu2oDb5%2FiTkz5N%2F9x%2FWmvxFfLo2kisd%2BOU9Xjo%2BiQkPw2ncKDiYRKWy870kdeNZUeQmAC7odaUY8%2FzQVuSFzxwAPW0oP8Menvjz5P7RKlWIA";
        window.__genspark_locale = "en-US";
        window.__genspark_token = "To/BnjzloZ3UfQdcSaYfDlLj8PV8RWu7NFfUUc8UudsCksmSxbrrylIy4Cd95Lj1I1UR2gonTplmajUQRnY3nZ6/vx0Xlf5AHpgCLHCZmc6mPTiZVnVMYKHsCdCAPniw76HCIoAEPwvlztmNP9vjmxErnt+gM5Ny9ISxoTjx/i7DQSt4i5yFXVCY+ZP8QOqWfpWqOofqYG6nGzeKtTHHDeH0wotDttqicbn3KrV55knYzMFtGUpmdYV7Au7s7OeHG4AP7QFkqJzMYvKDGxm6uyyXHxyq6ipv6DEMzOquBoxSqdHqxOso2gTs7eByEai04PccGPuyBFDBWyfmlnEngJLBatgXeR7xhFkLqw/cpbhEt514sTGWinBrkjkErBua5p2/30l8jyBmYdFfnMBFTu2oDb5/iTkz5N/9x/WmvxFfLo2kisd+OU9Xjo+iQkPw2ncKDiYRKWy870kdeNZUeQmAC7odaUY8/zQVuSFzxwAPW0oP8Menvjz5P7RKlWIA";
    </script>
    
    <script id="html_notice_dialog_script" src="https://www.genspark.ai/notice_dialog.js"></script>
    