📦 package.json
{
  "name": "@figma/my-make-file",
  "private": true,
  "version": "0.0.1",
  "type": "module",
  "scripts": {
    "build": "vite build"
  },
  "dependencies": {
    "@emotion/react": "11.14.0",
    "@emotion/styled": "11.14.1",
    "@mui/icons-material": "7.3.5",
    "@mui/material": "7.3.5",
    "@popperjs/core": "2.11.8",
    "@radix-ui/react-accordion": "1.2.3",
    "@radix-ui/react-alert-dialog": "1.1.6",
    "@radix-ui/react-aspect-ratio": "1.1.2",
    "@radix-ui/react-avatar": "1.1.3",
    "@radix-ui/react-checkbox": "1.1.4",
    "@radix-ui/react-collapsible": "1.1.3",
    "@radix-ui/react-context-menu": "2.2.6",
    "@radix-ui/react-dialog": "1.1.6",
    "@radix-ui/react-dropdown-menu": "2.1.6",
    "@radix-ui/react-hover-card": "1.1.6",
    "@radix-ui/react-label": "2.1.2",
    "@radix-ui/react-menubar": "1.1.6",
    "@radix-ui/react-navigation-menu": "1.2.5",
    "@radix-ui/react-popover": "1.1.6",
    "@radix-ui/react-progress": "1.1.2",
    "@radix-ui/react-radio-group": "1.2.3",
    "@radix-ui/react-scroll-area": "1.2.3",
    "@radix-ui/react-select": "2.1.6",
    "@radix-ui/react-separator": "1.1.2",
    "@radix-ui/react-slider": "1.2.3",
    "@radix-ui/react-slot": "1.1.2",
    "@radix-ui/react-switch": "1.1.3",
    "@radix-ui/react-tabs": "1.1.3",
    "@radix-ui/react-toggle-group": "1.1.2",
    "@radix-ui/react-toggle": "1.1.2",
    "@radix-ui/react-tooltip": "1.1.8",
    "canvas-confetti": "1.9.4",
    "class-variance-authority": "0.7.1",
    "clsx": "2.1.1",
    "cmdk": "1.1.1",
    "date-fns": "3.6.0",
    "embla-carousel-react": "8.6.0",
    "input-otp": "1.4.2",
    "lucide-react": "0.487.0",
    "motion": "12.23.24",
    "next-themes": "0.4.6",
    "react-day-picker": "8.10.1",
    "react-dnd": "16.0.1",
    "react-dnd-html5-backend": "16.0.1",
    "react-hook-form": "7.55.0",
    "react-popper": "2.3.0",
    "react-resizable-panels": "2.1.7",
    "react-responsive-masonry": "2.7.1",
    "react-router": "7.13.0",
    "react-slick": "0.31.0",
    "recharts": "2.15.2",
    "sonner": "2.0.3",
    "tailwind-merge": "3.2.0",
    "tw-animate-css": "1.3.8",
    "vaul": "1.1.2"
  },
  "devDependencies": {
    "@tailwindcss/vite": "4.1.12",
    "@vitejs/plugin-react": "4.7.0",
    "tailwindcss": "4.1.12",
    "vite": "6.3.5"
  },
  "peerDependencies": {
    "react": "18.3.1",
    "react-dom": "18.3.1"
  },
  "peerDependenciesMeta": {
    "react": {
      "optional": true
    },
    "react-dom": {
      "optional": true
    }
  },
  "pnpm": {
    "overrides": {
      "vite": "6.3.5"
    }
  }
}
⚙️ vite.config.ts
import { defineConfig } from 'vite'
import path from 'path'
import tailwindcss from '@tailwindcss/vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [
    react(),
    tailwindcss(),
  ],
  resolve: {
    alias: {
      '@': path.resolve(__dirname, './src'),
    },
  },
  assetsInclude: ['**/*.svg', '**/*.csv'],
})
🎨 src/styles/theme.css
@custom-variant dark (&:is(.dark *));

:root {
  --font-size: 16px;
  --background: #F5EBE8;
  --foreground: #6B5448;
  --card: #ffffff;
  --card-foreground: #6B5448;
  --popover: #ffffff;
  --popover-foreground: #6B5448;
  --primary: #C7998E;
  --primary-foreground: #ffffff;
  --secondary: #E8D5D0;
  --secondary-foreground: #6B5448;
  --muted: #D4B5AB;
  --muted-foreground: #8B7367;
  --accent: #B8897C;
  --accent-foreground: #ffffff;
  --destructive: #C17C74;
  --destructive-foreground: #ffffff;
  --border: rgba(199, 153, 142, 0.2);
  --input: transparent;
  --input-background: #ffffff;
  --switch-background: #D4B5AB;
  --font-weight-medium: 500;
  --font-weight-normal: 400;
  --ring: #C7998E;
  --chart-1: oklch(0.646 0.222 41.116);
  --chart-2: oklch(0.6 0.118 184.704);
  --chart-3: oklch(0.398 0.07 227.392);
  --chart-4: oklch(0.828 0.189 84.429);
  --chart-5: oklch(0.769 0.188 70.08);
  --radius: 1.5rem;
  --sidebar: #F5EBE8;
  --sidebar-foreground: #6B5448;
  --sidebar-primary: #C7998E;
  --sidebar-primary-foreground: #ffffff;
  --sidebar-accent: #E8D5D0;
  --sidebar-accent-foreground: #6B5448;
  --sidebar-border: #D4B5AB;
  --sidebar-ring: #C7998E;

  /* Paleta nude/beige/rosada elegante */
  --nude-lightest: #F9F3F0;
  --nude-light: #F5EBE8;
  --nude-medium: #E8D5D0;
  --nude-rose: #DCC4BE;
  --nude-dark: #D4B5AB;
  --taupe-light: #E5D7D2;
  --taupe-medium: #C7B0A6;
  --mauve: #C7998E;
  --mauve-dark: #B8897C;
  --brown-text: #6B5448;
  --brown-light: #8B7367;
  --cream: #FAF6F4;
}

.dark {
  --background: oklch(0.145 0 0);
  --foreground: oklch(0.985 0 0);
  --card: oklch(0.145 0 0);
  --card-foreground: oklch(0.985 0 0);
  --popover: oklch(0.145 0 0);
  --popover-foreground: oklch(0.985 0 0);
  --primary: oklch(0.985 0 0);
  --primary-foreground: oklch(0.205 0 0);
  --secondary: oklch(0.269 0 0);
  --secondary-foreground: oklch(0.985 0 0);
  --muted: oklch(0.269 0 0);
  --muted-foreground: oklch(0.708 0 0);
  --accent: oklch(0.269 0 0);
  --accent-foreground: oklch(0.985 0 0);
  --destructive: oklch(0.396 0.141 25.723);
  --destructive-foreground: oklch(0.637 0.237 25.331);
  --border: oklch(0.269 0 0);
  --input: oklch(0.269 0 0);
  --ring: oklch(0.439 0 0);
  --font-weight-medium: 500;
  --font-weight-normal: 400;
  --chart-1: oklch(0.488 0.243 264.376);
  --chart-2: oklch(0.696 0.17 162.48);
  --chart-3: oklch(0.769 0.188 70.08);
  --chart-4: oklch(0.627 0.265 303.9);
  --chart-5: oklch(0.645 0.246 16.439);
  --sidebar: oklch(0.205 0 0);
  --sidebar-foreground: oklch(0.985 0 0);
  --sidebar-primary: oklch(0.488 0.243 264.376);
  --sidebar-primary-foreground: oklch(0.985 0 0);
  --sidebar-accent: oklch(0.269 0 0);
  --sidebar-accent-foreground: oklch(0.985 0 0);
  --sidebar-border: oklch(0.269 0 0);
  --sidebar-ring: oklch(0.439 0 0);
}

@theme inline {
  --color-background: var(--background);
  --color-foreground: var(--foreground);
  --color-card: var(--card);
  --color-card-foreground: var(--card-foreground);
  --color-popover: var(--popover);
  --color-popover-foreground: var(--popover-foreground);
  --color-primary: var(--primary);
  --color-primary-foreground: var(--primary-foreground);
  --color-secondary: var(--secondary);
  --color-secondary-foreground: var(--secondary-foreground);
  --color-muted: var(--muted);
  --color-muted-foreground: var(--muted-foreground);
  --color-accent: var(--accent);
  --color-accent-foreground: var(--accent-foreground);
  --color-destructive: var(--destructive);
  --color-destructive-foreground: var(--destructive-foreground);
  --color-border: var(--border);
  --color-input: var(--input);
  --color-input-background: var(--input-background);
  --color-switch-background: var(--switch-background);
  --color-ring: var(--ring);
  --color-chart-1: var(--chart-1);
  --color-chart-2: var(--chart-2);
  --color-chart-3: var(--chart-3);
  --color-chart-4: var(--chart-4);
  --color-chart-5: var(--chart-5);
  --radius-sm: calc(var(--radius) - 4px);
  --radius-md: calc(var(--radius) - 2px);
  --radius-lg: var(--radius);
  --radius-xl: calc(var(--radius) + 4px);
  --color-sidebar: var(--sidebar);
  --color-sidebar-foreground: var(--sidebar-foreground);
  --color-sidebar-primary: var(--sidebar-primary);
  --color-sidebar-primary-foreground: var(--sidebar-primary-foreground);
  --color-sidebar-accent: var(--sidebar-accent);
  --color-sidebar-accent-foreground: var(--sidebar-accent-foreground);
  --color-sidebar-border: var(--sidebar-border);
  --color-sidebar-ring: var(--sidebar-ring);
}

@layer base {
  * {
    @apply border-border outline-ring/50;
  }

  body {
    @apply bg-background text-foreground;
  }

  html {
    font-size: var(--font-size);
  }

  h1 {
    font-size: var(--text-2xl);
    font-weight: var(--font-weight-medium);
    line-height: 1.5;
  }

  h2 {
    font-size: var(--text-xl);
    font-weight: var(--font-weight-medium);
    line-height: 1.5;
  }

  h3 {
    font-size: var(--text-lg);
    font-weight: var(--font-weight-medium);
    line-height: 1.5;
  }

  h4 {
    font-size: var(--text-base);
    font-weight: var(--font-weight-medium);
    line-height: 1.5;
  }

  label {
    font-size: var(--text-base);
    font-weight: var(--font-weight-medium);
    line-height: 1.5;
  }

  button {
    font-size: var(--text-base);
    font-weight: var(--font-weight-medium);
    line-height: 1.5;
  }

  input {
    font-size: var(--text-base);
    font-weight: var(--font-weight-normal);
    line-height: 1.5;
  }
}
⚛️ src/app/App.tsx
import { Header } from "./components/Header";
import { Hero } from "./components/Hero";
import { TrustBadges } from "./components/TrustBadges";
import { Collections } from "./components/Collections";
import { Customize } from "./components/Customize";
import { Sustainability } from "./components/Sustainability";
import { Testimonials } from "./components/Testimonials";
import { HowToBuy } from "./components/HowToBuy";
import { PaymentShipping } from "./components/PaymentShipping";
import { FAQ } from "./components/FAQ";
import { Newsletter } from "./components/Newsletter";
import { Footer } from "./components/Footer";
import { WhatsAppButton } from "./components/WhatsAppButton";
import { Chatbot } from "./components/Chatbot";
import { Analytics } from "./components/Analytics";

export default function App() {
  return (
    <div className="min-h-screen flex flex-col">
      <Analytics />
      <Header />
      <main className="flex-1">
        <Hero />
        <TrustBadges />
        <Collections />
        <Customize />
        <Sustainability />
        <Testimonials />
        <HowToBuy />
        <PaymentShipping />
        <FAQ />
        <Newsletter />
      </main>
      <Footer />
      <WhatsAppButton />
      <Chatbot />
    </div>
  );
}
📱 COMPONENTES - Parte 1
src/app/components/Header.tsx
import { Menu, ShoppingBag, Sparkles } from "lucide-react";
import { useState } from "react";

export function Header() {
  const [menuOpen, setMenuOpen] = useState(false);
  const whatsappNumber = "3203575433";

  const handleBuyNow = () => {
    const message = "¡Hola! Quiero comprar uñas press-on de Nära Nails 💅";
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
    window.open(url, "_blank");
  };

  return (
    <header className="sticky top-0 z-50 w-full backdrop-blur-sm border-b" style={{ backgroundColor: 'rgba(255, 255, 255, 0.95)', borderColor: '#E8D5D0' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="flex items-center justify-between h-16 md:h-20">
          <div className="flex items-center gap-2">
            <Sparkles className="w-6 h-6" style={{ color: '#C7998E' }} />
            <span className="font-semibold text-xl" style={{ color: '#C7998E' }}>Nära Nails</span>
          </div>

          <nav className="hidden md:flex items-center gap-8">
            <a href="#inicio" className="transition-colors" style={{ color: '#6B5448' }}>
              Inicio
            </a>
            <a href="#colecciones" className="transition-colors" style={{ color: '#6B5448' }}>
              Colecciones
            </a>
            <a href="#personaliza" className="transition-colors" style={{ color: '#6B5448' }}>
              Personaliza
            </a>
            <a href="#como-comprar" className="transition-colors" style={{ color: '#6B5448' }}>
              Cómo Comprar
            </a>
          </nav>

          <div className="flex items-center gap-4">
            <button
              onClick={handleBuyNow}
              className="hidden md:flex items-center gap-2 px-6 py-2.5 text-white rounded-full transition-colors"
              style={{ backgroundColor: '#C7998E' }}
            >
              <ShoppingBag className="w-4 h-4" />
              Comprar Ahora
            </button>

            <button
              onClick={() => setMenuOpen(!menuOpen)}
              className="md:hidden p-2 text-foreground hover:text-primary"
              aria-label="Toggle menu"
            >
              <Menu className="w-6 h-6" />
            </button>
          </div>
        </div>

        {menuOpen && (
          <nav className="md:hidden pb-4 flex flex-col gap-4">
            <a
              href="#inicio"
              onClick={() => setMenuOpen(false)}
              className="text-foreground hover:text-primary transition-colors py-2"
            >
              Inicio
            </a>
            <a
              href="#colecciones"
              onClick={() => setMenuOpen(false)}
              className="text-foreground hover:text-primary transition-colors py-2"
            >
              Colecciones
            </a>
            <a
              href="#personaliza"
              onClick={() => setMenuOpen(false)}
              className="text-foreground hover:text-primary transition-colors py-2"
            >
              Personaliza
            </a>
            <a
              href="#como-comprar"
              onClick={() => setMenuOpen(false)}
              className="text-foreground hover:text-primary transition-colors py-2"
            >
              Cómo Comprar
            </a>
            <button
              onClick={handleBuyNow}
              className="flex items-center justify-center gap-2 px-6 py-2.5 bg-primary text-white rounded-full hover:bg-pink-600 transition-colors"
            >
              <ShoppingBag className="w-4 h-4" />
              Comprar Ahora
            </button>
          </nav>
        )}
      </div>
    </header>
  );
}
src/app/components/Hero.tsx
import { Sparkles, Heart } from "lucide-react";
import heroImage from "../../imports/WhatsApp_Image_2026-05-19_at_3.02.21_PM.jpeg";

export function Hero() {
  const scrollToCollections = () => {
    document.getElementById('colecciones')?.scrollIntoView({ behavior: 'smooth' });
  };
  return (
    <section id="inicio" className="relative py-16 md:py-24 lg:py-32 overflow-hidden" style={{ backgroundColor: '#F5EBE8' }}>
      <div className="absolute inset-0 bg-gradient-to-br from-[#F9F3F0]/50 via-[#F5EBE8]/30 to-[#E8D5D0]/40" />

      <div className="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        <div className="grid md:grid-cols-2 gap-12 items-center">
          <div className="space-y-6 md:space-y-8">
            <div className="inline-flex items-center gap-2 px-4 py-2 rounded-full" style={{ backgroundColor: '#E8D5D0' }}>
              <Heart className="w-4 h-4 fill-current" style={{ color: '#C7998E' }} />
              <span className="text-sm" style={{ color: '#C7998E' }}>Uñas Press-On Personalizadas</span>
            </div>

            <h1 className="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight" style={{ color: '#6B5448' }}>
              ¿También quieres verte arreglada{" "}
              <span style={{ color: '#C7998E' }}>sin perder tiempo?</span>
            </h1>

            <p className="text-lg md:text-xl max-w-xl" style={{ color: '#8B7367' }}>
              Descubre tu momento de autocuidado y practicidad. Nuestra colección de uñas press-on se aplica en minutos. Perfectas para la mujer moderna que valora su tiempo.
            </p>

            <div className="flex flex-col sm:flex-row gap-4">
              <button
                onClick={scrollToCollections}
                className="inline-flex items-center justify-center gap-2 px-8 py-4 text-white rounded-full transition-all hover:scale-105"
                style={{ backgroundColor: '#C7998E' }}
              >
                <Sparkles className="w-5 h-5" />
                Conoce Nära Nails
              </button>
              <button
                onClick={scrollToCollections}
                className="inline-flex items-center justify-center gap-2 px-8 py-4 bg-white rounded-full border-2 transition-colors"
                style={{ color: '#C7998E', borderColor: '#C7998E' }}
              >
                Ver Colección
              </button>
            </div>

            <div className="grid grid-cols-3 gap-6 pt-8 border-t" style={{ borderColor: '#D4B5AB' }}>
              <div>
                <div className="text-2xl md:text-3xl font-bold" style={{ color: '#C7998E' }}>100%</div>
                <div className="text-sm" style={{ color: '#8B7367' }}>Personalizable</div>
              </div>
              <div>
                <div className="text-2xl md:text-3xl font-bold" style={{ color: '#C7998E' }}>24/7</div>
                <div className="text-sm" style={{ color: '#8B7367' }}>Envío Express</div>
              </div>
              <div>
                <div className="text-2xl md:text-3xl font-bold" style={{ color: '#C7998E' }}>500+</div>
                <div className="text-sm" style={{ color: '#8B7367' }}>Diseños Únicos</div>
              </div>
            </div>
          </div>

          <div className="relative">
            <div className="relative rounded-3xl overflow-hidden shadow-2xl">
              <img
                src={heroImage}
                alt="Nära Nails - Descubre tu momento de autocuidado y practicidad"
                className="w-full h-auto"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-[#6B5448]/10 to-transparent" />
            </div>

            <div className="absolute -bottom-6 -right-6 w-32 h-32 rounded-full blur-3xl opacity-20" style={{ backgroundColor: '#C7998E' }} />
            <div className="absolute -top-6 -left-6 w-40 h-40 rounded-full blur-3xl opacity-20" style={{ backgroundColor: '#D4B5AB' }} />
          </div>
        </div>
      </div>
    </section>
  );
}
src/app/components/TrustBadges.tsx
import { Shield, Truck, CreditCard, Award, Lock, Package } from "lucide-react";

export function TrustBadges() {
  const badges = [
    {
      icon: Shield,
      title: "Compra Segura",
      description: "SSL 256-bit"
    },
    {
      icon: Truck,
      title: "Envío Express",
      description: "24-48h Interrapidísimo"
    },
    {
      icon: CreditCard,
      title: "Pago Protegido",
      description: "MercadoPago"
    },
    {
      icon: Package,
      title: "Devoluciones",
      description: "30 días garantía"
    },
    {
      icon: Award,
      title: "Calidad Premium",
      description: "Certificado ISO"
    },
    {
      icon: Lock,
      title: "Privacidad",
      description: "Datos protegidos"
    }
  ];

  return (
    <section className="py-12 border-y" style={{ backgroundColor: '#F9F3F0', borderColor: '#E8D5D0' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-6">
          {badges.map((badge, index) => {
            const Icon = badge.icon;
            return (
              <div key={index} className="flex flex-col items-center text-center gap-2">
                <div className="w-12 h-12 rounded-full flex items-center justify-center" style={{ backgroundColor: 'rgba(199, 153, 142, 0.1)' }}>
                  <Icon className="w-6 h-6" style={{ color: '#C7998E' }} />
                </div>
                <div>
                  <div className="font-semibold text-sm" style={{ color: '#6B5448' }}>{badge.title}</div>
                  <div className="text-xs" style={{ color: '#8B7367' }}>{badge.description}</div>
                </div>
              </div>
            );
          })}
        </div>
      </div>
    </section>
  );
}
src/app/components/Collections.tsx
import { useState } from "react";
import { ProductModal } from "./ProductModal";

export function Collections() {
  const [selectedProduct, setSelectedProduct] = useState<any>(null);

  const collections = [
    {
      title: "Romance Rosa",
      image:
        "https://images.unsplash.com/photo-1643648854897-7b5845b4c04c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=600",
      description: "Tonos suaves y románticos perfectos para looks delicados",
      price: "$35.000",
      features: [
        "10 uñas press-on premium",
        "Adhesivos premium de larga duración",
        "Lima profesional incluida",
        "Guía de aplicación paso a paso",
        "Reutilizables hasta 3 veces",
        "Duración: 1-2 semanas"
      ]
    },
    {
      title: "Elegancia Natural",
      image:
        "https://images.unsplash.com/photo-1633955726992-2b7c0d2d2a69?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=600",
      description: "Minimalista y sofisticado para uso diario",
      price: "$30.000",
      features: [
        "10 uñas press-on premium",
        "Adhesivos premium de larga duración",
        "Lima profesional incluida",
        "Guía de aplicación paso a paso",
        "Reutilizables hasta 3 veces",
        "Duración: 1-2 semanas"
      ]
    },
    {
      title: "French Clásico",
      image:
        "https://images.unsplash.com/photo-1604902396830-aca29e19b067?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=600",
      description: "Francés elegante perfecto para toda ocasión",
      price: "$42.000",
      features: [
        "10 uñas con diseño francés",
        "Adhesivos premium de larga duración",
        "Lima profesional incluida",
        "Guía de aplicación paso a paso",
        "Reutilizables hasta 3 veces",
        "Duración: 1-2 semanas"
      ]
    },
    {
      title: "Nude Chic",
      image:
        "https://images.unsplash.com/photo-1680540555907-c99c665a20b7?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=600",
      description: "Clásico y atemporal para oficina",
      price: "$32.000",
      features: [
        "10 uñas press-on premium",
        "Adhesivos premium de larga duración",
        "Lima profesional incluida",
        "Guía de aplicación paso a paso",
        "Reutilizables hasta 3 veces",
        "Duración: 1-2 semanas"
      ]
    },
    {
      title: "Stiletto Glam",
      image:
        "https://images.unsplash.com/photo-1610992015836-7c249d75782d?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=600",
      description: "Forma stiletto con acabado brillante y atrevido",
      price: "$48.000",
      features: [
        "10 uñas stiletto premium",
        "Diseño moderno y elegante",
        "Adhesivos premium de larga duración",
        "Lima profesional incluida",
        "Guía de aplicación paso a paso",
        "Duración: 1-2 semanas"
      ]
    },
    {
      title: "Arte Floral",
      image:
        "https://images.unsplash.com/photo-1690749072212-373daf1d58ca?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=600",
      description: "Diseños florales exclusivos pintados a mano",
      price: "$60.000",
      features: [
        "10 uñas con arte nail exclusivo",
        "Diseño floral pintado a mano",
        "Piedras y decoraciones premium",
        "Adhesivos premium de larga duración",
        "Lima profesional incluida",
        "Reutilizables hasta 2 veces"
      ]
    },
  ];

  return (
    <section id="colecciones" className="py-16 md:py-24" style={{ backgroundColor: '#F5EBE8' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-12 md:mb-16">
          <h2 className="text-3xl md:text-4xl lg:text-5xl font-bold mb-4" style={{ color: '#6B5448' }}>
            Nuestras Colecciones
          </h2>
          <p className="text-lg max-w-2xl mx-auto" style={{ color: '#8B7367' }}>
            Explora nuestra selección curada de diseños exclusivos. Cada set incluye 24 uñas en
            diferentes tamaños para un ajuste perfecto.
          </p>
        </div>

        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
          {collections.map((collection, index) => (
            <div
              key={index}
              className="group relative overflow-hidden rounded-2xl hover:shadow-xl transition-all duration-300 cursor-pointer bg-white"
            >
              <div className="aspect-[3/4] overflow-hidden">
                <img
                  src={collection.image}
                  alt={collection.title}
                  className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
                />
              </div>

              <div className="p-6">
                <h3 className="text-xl font-semibold mb-2" style={{ color: '#6B5448' }}>
                  {collection.title}
                </h3>
                <p className="text-sm mb-3" style={{ color: '#8B7367' }}>
                  {collection.description}
                </p>
                <p className="text-2xl font-bold mb-4" style={{ color: '#C7998E' }}>
                  {collection.price}
                </p>
                <button
                  onClick={() => setSelectedProduct(collection)}
                  className="w-full py-3 text-white rounded-full transition-all hover:scale-105"
                  style={{ backgroundColor: '#C7998E' }}
                >
                  Ver Detalles y Comprar
                </button>
              </div>
            </div>
          ))}
        </div>

        <div className="text-center mt-12">
          <a href="#colecciones">
            <button className="px-8 py-4 text-white rounded-full transition-colors" style={{ backgroundColor: '#C7998E' }}>
              Ver Todas las Colecciones
            </button>
          </a>
        </div>
      </div>

      <ProductModal
        isOpen={!!selectedProduct}
        onClose={() => setSelectedProduct(null)}
        product={selectedProduct || collections[0]}
      />
    </section>
  );
}
📱 COMPONENTES - Parte 2
src/app/components/ProductModal.tsx
import { X, ShoppingCart, Heart } from "lucide-react";
import { useState } from "react";

interface ProductModalProps {
  isOpen: boolean;
  onClose: () => void;
  product: {
    title: string;
    image: string;
    description: string;
    price: string;
    features: string[];
  };
}

export function ProductModal({ isOpen, onClose, product }: ProductModalProps) {
  const [quantity, setQuantity] = useState(1);
  const whatsappNumber = "3203575433";

  const handleBuyNow = () => {
    const priceValue = parseInt(product.price.replace(/[$.]/g, ''));
    const total = priceValue * quantity;
    const message = `¡Hola! Quiero comprar ${quantity} set(s) de ${product.title} (${product.price} c/u). Total: $${total.toLocaleString('es-CO')} COP`;
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
    window.open(url, "_blank");
  };

  if (!isOpen) return null;

  return (
    <div className="fixed inset-0 z-[100] flex items-center justify-center p-4 bg-black/50 backdrop-blur-sm animate-in fade-in">
      <div className="bg-white rounded-3xl max-w-2xl w-full max-h-[90vh] overflow-y-auto shadow-2xl animate-in slide-in-from-bottom-4">
        <div className="sticky top-0 bg-white border-b border-gray-100 p-4 flex items-center justify-between">
          <h2 className="text-xl font-bold" style={{ color: '#6B5448' }}>{product.title}</h2>
          <button
            onClick={onClose}
            className="w-10 h-10 rounded-full hover:bg-gray-100 flex items-center justify-center transition-colors"
          >
            <X className="w-5 h-5" />
          </button>
        </div>

        <div className="p-6">
          <div className="mb-6">
            <img
              src={product.image}
              alt={product.title}
              className="w-full rounded-2xl shadow-lg"
            />
          </div>

          <div className="mb-6">
            <div className="flex items-center justify-between mb-4">
              <div>
                <p className="text-3xl font-bold" style={{ color: '#C7998E' }}>{product.price}</p>
                <p className="text-sm" style={{ color: '#8B7367' }}>IVA incluido</p>
              </div>
              <button className="w-12 h-12 rounded-full border-2 flex items-center justify-center transition-colors" style={{ borderColor: '#C7998E' }}>
                <Heart className="w-6 h-6" style={{ color: '#C7998E' }} />
              </button>
            </div>

            <p className="text-lg mb-4" style={{ color: '#6B5448' }}>{product.description}</p>

            <div className="bg-gray-50 rounded-xl p-4 mb-6">
              <h3 className="font-semibold mb-3" style={{ color: '#6B5448' }}>✨ Incluye:</h3>
              <ul className="space-y-2">
                {product.features.map((feature, index) => (
                  <li key={index} className="flex items-start gap-2 text-sm" style={{ color: '#8B7367' }}>
                    <span className="text-green-600 mt-0.5">✓</span>
                    <span>{feature}</span>
                  </li>
                ))}
              </ul>
            </div>

            <div className="flex items-center gap-4 mb-6">
              <label className="font-semibold" style={{ color: '#6B5448' }}>Cantidad:</label>
              <div className="flex items-center gap-3">
                <button
                  onClick={() => setQuantity(Math.max(1, quantity - 1))}
                  className="w-10 h-10 rounded-full flex items-center justify-center transition-colors"
                  style={{ backgroundColor: '#E8D5D0' }}
                >
                  -
                </button>
                <span className="text-xl font-bold w-8 text-center" style={{ color: '#6B5448' }}>{quantity}</span>
                <button
                  onClick={() => setQuantity(quantity + 1)}
                  className="w-10 h-10 rounded-full flex items-center justify-center transition-colors"
                  style={{ backgroundColor: '#E8D5D0' }}
                >
                  +
                </button>
              </div>
            </div>

            <button
              onClick={handleBuyNow}
              className="w-full py-4 text-white rounded-full flex items-center justify-center gap-2 transition-all hover:scale-105"
              style={{ backgroundColor: '#C7998E' }}
            >
              <ShoppingCart className="w-5 h-5" />
              Comprar por WhatsApp
            </button>

            <p className="text-xs text-center mt-4" style={{ color: '#8B7367' }}>
              🚚 Envío GRATIS en compras superiores a $80.000 COP
            </p>
          </div>
        </div>
      </div>
    </div>
  );
}
src/app/components/Customize.tsx
import { Palette, Ruler, Sparkles, Package } from "lucide-react";
import { useState } from "react";
import { CustomizeModal } from "./CustomizeModal";

export function Customize() {
  const [showCustomizeModal, setShowCustomizeModal] = useState(false);
  const features = [
    {
      icon: Palette,
      title: "Elige tu Estilo",
      description:
        "Selecciona entre cientos de colores, acabados y diseños. Desde nude elegante hasta glitter vibrante.",
    },
    {
      icon: Ruler,
      title: "Tamaño Perfecto",
      description:
        "10 uñas press-on premium diseñadas para ajuste perfecto. Encuentra tu estilo ideal.",
    },
    {
      icon: Sparkles,
      title: "Diseños Únicos",
      description:
        "Personaliza con arte nail exclusivo, piedras, efectos cromados y acabados mate o brillante.",
    },
    {
      icon: Package,
      title: "Kit Completo",
      description:
        "Recibe todo lo necesario: uñas, adhesivos premium, lima y guía de aplicación paso a paso.",
    },
  ];

  return (
    <section id="personaliza" className="py-16 md:py-24" style={{ backgroundColor: '#E8D5D0' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid md:grid-cols-2 gap-12 items-center mb-16">
          <div>
            <h2 className="text-3xl md:text-4xl lg:text-5xl font-bold text-foreground mb-6">
              Personalización a Tu Medida
            </h2>
            <p className="text-lg text-muted-foreground mb-8">
              Crea uñas que reflejen tu estilo único. Nuestro sistema de personalización te permite
              diseñar el set perfecto según tus preferencias. Calidad de salón, comodidad de casa.
            </p>
            <div className="space-y-4">
              <div className="flex items-start gap-4">
                <div className="w-8 h-8 rounded-full bg-primary/10 flex items-center justify-center flex-shrink-0 mt-1">
                  <span className="text-primary font-semibold">1</span>
                </div>
                <div>
                  <h3 className="font-semibold text-foreground mb-1">
                    Selecciona tu Forma y Largo
                  </h3>
                  <p className="text-sm text-muted-foreground">
                    10 uñas premium. Ovalada, cuadrada, almendrada o stiletto. Corta, media o larga.
                  </p>
                </div>
              </div>
              <div className="flex items-start gap-4">
                <div className="w-8 h-8 rounded-full bg-primary/10 flex items-center justify-center flex-shrink-0 mt-1">
                  <span className="text-primary font-semibold">2</span>
                </div>
                <div>
                  <h3 className="font-semibold text-foreground mb-1">Elige Color y Acabado</h3>
                  <p className="text-sm text-muted-foreground">
                    Mate, brillante, cromado, holográfico o degradado.
                  </p>
                </div>
              </div>
              <div className="flex items-start gap-4">
                <div className="w-8 h-8 rounded-full bg-primary/10 flex items-center justify-center flex-shrink-0 mt-1">
                  <span className="text-primary font-semibold">3</span>
                </div>
                <div>
                  <h3 className="font-semibold text-foreground mb-1">Añade Diseño Personalizado</h3>
                  <p className="text-sm text-muted-foreground">
                    Stones, arte nail, francés, ombré y más opciones premium.
                  </p>
                </div>
              </div>
            </div>
            <button
              onClick={() => setShowCustomizeModal(true)}
              className="mt-8 px-8 py-4 bg-primary text-white rounded-full hover:bg-pink-600 transition-colors"
            >
              Empieza a Personalizar
            </button>
          </div>

          <div className="relative">
            <img
              src="https://images.unsplash.com/photo-1690749072212-373daf1d58ca?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&q=80&w=800"
              alt="Personalización de uñas"
              className="rounded-3xl shadow-2xl w-full"
            />
            <div className="absolute -bottom-8 -left-8 w-64 h-64 bg-primary rounded-full blur-3xl opacity-10" />
          </div>
        </div>

        <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-6 md:gap-8">
          {features.map((feature, index) => {
            const Icon = feature.icon;
            return (
              <div
                key={index}
                className="bg-white rounded-2xl p-6 shadow-sm hover:shadow-lg transition-shadow"
              >
                <div className="w-12 h-12 rounded-xl bg-secondary flex items-center justify-center mb-4">
                  <Icon className="w-6 h-6 text-primary" />
                </div>
                <h3 className="font-semibold text-foreground mb-2">{feature.title}</h3>
                <p className="text-sm text-muted-foreground">{feature.description}</p>
              </div>
            );
          })}
        </div>
      </div>

      <CustomizeModal
        isOpen={showCustomizeModal}
        onClose={() => setShowCustomizeModal(false)}
      />
    </section>
  );
}
src/app/components/CustomizeModal.tsx
import { X, ArrowRight } from "lucide-react";
import { useState } from "react";

interface CustomizeModalProps {
  isOpen: boolean;
  onClose: () => void;
}

export function CustomizeModal({ isOpen, onClose }: CustomizeModalProps) {
  const [step, setStep] = useState(1);
  const [selections, setSelections] = useState({
    shape: "",
    length: "",
    color: "",
    finish: "",
    design: ""
  });

  const whatsappNumber = "3203575433";

  const shapes = ["Ovalada", "Cuadrada", "Almendrada", "Stiletto", "Bailarina"];
  const lengths = ["Corta", "Media", "Larga"];
  const colors = ["Nude", "Rosa", "Rojo", "Blanco", "Negro", "Degradado"];
  const finishes = ["Mate", "Brillante", "Cromado", "Holográfico"];
  const designs = ["Sin diseño", "Francés", "Ombré", "Piedras", "Arte Nail", "Glitter"];

  const handleFinish = () => {
    const message = `¡Hola! Quiero personalizar mis uñas press-on:\n\n` +
      `🔹 Forma: ${selections.shape}\n` +
      `🔹 Largo: ${selections.length}\n` +
      `🔹 Color: ${selections.color}\n` +
      `🔹 Acabado: ${selections.finish}\n` +
      `🔹 Diseño: ${selections.design}\n\n` +
      `¿Cuál sería el precio final?`;
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
    window.open(url, "_blank");
    onClose();
  };

  const isStepComplete = () => {
    switch (step) {
      case 1: return selections.shape && selections.length;
      case 2: return selections.color && selections.finish;
      case 3: return selections.design;
      default: return false;
    }
  };

  if (!isOpen) return null;

  return (
    <div className="fixed inset-0 z-[100] flex items-center justify-center p-4 bg-black/50 backdrop-blur-sm animate-in fade-in">
      <div className="bg-white rounded-3xl max-w-2xl w-full max-h-[90vh] overflow-y-auto shadow-2xl animate-in slide-in-from-bottom-4">
        <div className="sticky top-0 bg-white border-b border-gray-100 p-4 flex items-center justify-between">
          <h2 className="text-xl font-bold" style={{ color: '#6B5448' }}>
            Personaliza tus Uñas - Paso {step}/3
          </h2>
          <button
            onClick={onClose}
            className="w-10 h-10 rounded-full hover:bg-gray-100 flex items-center justify-center transition-colors"
          >
            <X className="w-5 h-5" />
          </button>
        </div>

        <div className="p-6">
          {/* Progress Bar */}
          <div className="mb-8">
            <div className="flex gap-2">
              {[1, 2, 3].map((s) => (
                <div
                  key={s}
                  className="flex-1 h-2 rounded-full transition-colors"
                  style={{ backgroundColor: s <= step ? '#C7998E' : '#E8D5D0' }}
                />
              ))}
            </div>
          </div>

          {/* Step 1: Forma y Largo */}
          {step === 1 && (
            <div className="space-y-6">
              <div>
                <h3 className="font-semibold mb-4" style={{ color: '#6B5448' }}>1. Selecciona la Forma</h3>
                <div className="grid grid-cols-2 sm:grid-cols-3 gap-3">
                  {shapes.map((shape) => (
                    <button
                      key={shape}
                      onClick={() => setSelections({ ...selections, shape })}
                      className="p-4 rounded-xl border-2 transition-all hover:scale-105"
                      style={{
                        borderColor: selections.shape === shape ? '#C7998E' : '#E8D5D0',
                        backgroundColor: selections.shape === shape ? '#FCE4EC' : 'white'
                      }}
                    >
                      {shape}
                    </button>
                  ))}
                </div>
              </div>

              <div>
                <h3 className="font-semibold mb-4" style={{ color: '#6B5448' }}>2. Selecciona el Largo</h3>
                <div className="grid grid-cols-3 gap-3">
                  {lengths.map((length) => (
                    <button
                      key={length}
                      onClick={() => setSelections({ ...selections, length })}
                      className="p-4 rounded-xl border-2 transition-all hover:scale-105"
                      style={{
                        borderColor: selections.length === length ? '#C7998E' : '#E8D5D0',
                        backgroundColor: selections.length === length ? '#FCE4EC' : 'white'
                      }}
                    >
                      {length}
                    </button>
                  ))}
                </div>
              </div>
            </div>
          )}

          {/* Step 2: Color y Acabado */}
          {step === 2 && (
            <div className="space-y-6">
              <div>
                <h3 className="font-semibold mb-4" style={{ color: '#6B5448' }}>3. Elige el Color</h3>
                <div className="grid grid-cols-2 sm:grid-cols-3 gap-3">
                  {colors.map((color) => (
                    <button
                      key={color}
                      onClick={() => setSelections({ ...selections, color })}
                      className="p-4 rounded-xl border-2 transition-all hover:scale-105"
                      style={{
                        borderColor: selections.color === color ? '#C7998E' : '#E8D5D0',
                        backgroundColor: selections.color === color ? '#FCE4EC' : 'white'
                      }}
                    >
                      {color}
                    </button>
                  ))}
                </div>
              </div>

              <div>
                <h3 className="font-semibold mb-4" style={{ color: '#6B5448' }}>4. Elige el Acabado</h3>
                <div className="grid grid-cols-2 gap-3">
                  {finishes.map((finish) => (
                    <button
                      key={finish}
                      onClick={() => setSelections({ ...selections, finish })}
                      className="p-4 rounded-xl border-2 transition-all hover:scale-105"
                      style={{
                        borderColor: selections.finish === finish ? '#C7998E' : '#E8D5D0',
                        backgroundColor: selections.finish === finish ? '#FCE4EC' : 'white'
                      }}
                    >
                      {finish}
                    </button>
                  ))}
                </div>
              </div>
            </div>
          )}

          {/* Step 3: Diseño */}
          {step === 3 && (
            <div className="space-y-6">
              <div>
                <h3 className="font-semibold mb-4" style={{ color: '#6B5448' }}>5. Añade Diseño Personalizado</h3>
                <div className="grid grid-cols-2 sm:grid-cols-3 gap-3">
                  {designs.map((design) => (
                    <button
                      key={design}
                      onClick={() => setSelections({ ...selections, design })}
                      className="p-4 rounded-xl border-2 transition-all hover:scale-105"
                      style={{
                        borderColor: selections.design === design ? '#C7998E' : '#E8D5D0',
                        backgroundColor: selections.design === design ? '#FCE4EC' : 'white'
                      }}
                    >
                      {design}
                    </button>
                  ))}
                </div>
              </div>

              <div className="bg-gray-50 rounded-xl p-6">
                <h4 className="font-semibold mb-3" style={{ color: '#6B5448' }}>📋 Resumen de tu Personalización:</h4>
                <ul className="space-y-2 text-sm" style={{ color: '#8B7367' }}>
                  <li>🔹 Forma: <strong>{selections.shape}</strong></li>
                  <li>🔹 Largo: <strong>{selections.length}</strong></li>
                  <li>🔹 Color: <strong>{selections.color}</strong></li>
                  <li>🔹 Acabado: <strong>{selections.finish}</strong></li>
                  <li>🔹 Diseño: <strong>{selections.design}</strong></li>
                </ul>
              </div>
            </div>
          )}

          {/* Navigation Buttons */}
          <div className="flex gap-3 mt-8">
            {step > 1 && (
              <button
                onClick={() => setStep(step - 1)}
                className="flex-1 py-3 border-2 rounded-full transition-colors"
                style={{ borderColor: '#C7998E', color: '#C7998E' }}
              >
                Atrás
              </button>
            )}
            {step < 3 ? (
              <button
                onClick={() => setStep(step + 1)}
                disabled={!isStepComplete()}
                className="flex-1 py-3 text-white rounded-full flex items-center justify-center gap-2 transition-all disabled:opacity-50 disabled:cursor-not-allowed"
                style={{ backgroundColor: '#C7998E' }}
              >
                Siguiente
                <ArrowRight className="w-5 h-5" />
              </button>
            ) : (
              <button
                onClick={handleFinish}
                disabled={!isStepComplete()}
                className="flex-1 py-3 text-white rounded-full transition-all disabled:opacity-50 disabled:cursor-not-allowed"
                style={{ backgroundColor: '#C7998E' }}
              >
                Solicitar Cotización
              </button>
            )}
          </div>
        </div>
      </div>
    </div>
  );
}
📱 COMPONENTES - Parte 3
src/app/components/Sustainability.tsx
import { Leaf, Recycle, Heart, Award } from "lucide-react";

export function Sustainability() {
  const features = [
    {
      icon: Leaf,
      title: "Materiales Eco-Friendly",
      description: "Fabricadas con materiales no tóxicos y libres de químicos agresivos para tu salud y el planeta."
    },
    {
      icon: Recycle,
      title: "100% Reutilizables",
      description: "Nuestras uñas pueden usarse múltiples veces. Simplemente límpialas y vuelve a aplicarlas cuando quieras."
    },
    {
      icon: Heart,
      title: "Cruelty-Free",
      description: "Nunca testeado en animales. Productos veganos y certificados por asociaciones internacionales."
    },
    {
      icon: Award,
      title: "Empaquetado Sostenible",
      description: "Packaging biodegradable y minimalista. Cada detalle pensado para reducir nuestra huella de carbono."
    }
  ];

  return (
    <section className="py-16 md:py-24" style={{ backgroundColor: '#DCC4BE' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-12">
          <div className="inline-flex items-center gap-2 px-4 py-2 bg-green-100 rounded-full mb-4">
            <Leaf className="w-4 h-4 text-green-600" />
            <span className="text-sm text-green-700 font-medium">Compromiso Sostenible</span>
          </div>
          <h2 className="text-3xl md:text-4xl lg:text-5xl font-bold text-foreground mb-4">
            Belleza que Cuida el Planeta
          </h2>
          <p className="text-lg text-muted-foreground max-w-2xl mx-auto">
            En Nära Nails creemos que la belleza no debe costar al medio ambiente. Por eso cada producto
            está diseñado con conciencia ecológica y responsabilidad social.
          </p>
        </div>

        <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
          {features.map((feature, index) => {
            const Icon = feature.icon;
            return (
              <div
                key={index}
                className="bg-white rounded-2xl p-6 shadow-sm hover:shadow-md transition-shadow border border-green-100/50"
              >
                <div className="w-14 h-14 rounded-xl bg-green-100 flex items-center justify-center mb-4">
                  <Icon className="w-7 h-7 text-green-600" />
                </div>
                <h3 className="font-semibold text-foreground mb-2">{feature.title}</h3>
                <p className="text-sm text-muted-foreground">{feature.description}</p>
              </div>
            );
          })}
        </div>

        <div className="mt-12 bg-gradient-to-r from-green-500 to-emerald-600 rounded-3xl p-8 md:p-10 text-white text-center">
          <h3 className="text-2xl md:text-3xl font-bold mb-3">
            Nuestro Compromiso 2026
          </h3>
          <p className="text-lg mb-6 opacity-95 max-w-3xl mx-auto">
            Reducir en un 50% nuestras emisiones de carbono y plantar un árbol por cada 10 sets vendidos.
            Juntas hacemos la diferencia.
          </p>
          <div className="flex flex-wrap justify-center gap-8 text-center">
            <div>
              <div className="text-3xl font-bold">-50%</div>
              <div className="text-sm opacity-90">Emisiones CO₂</div>
            </div>
            <div className="w-px h-12 bg-white/30 hidden sm:block"></div>
            <div>
              <div className="text-3xl font-bold">1000+</div>
              <div className="text-sm opacity-90">Árboles Plantados</div>
            </div>
            <div className="w-px h-12 bg-white/30 hidden sm:block"></div>
            <div>
              <div className="text-3xl font-bold">100%</div>
              <div className="text-sm opacity-90">Packaging Reciclable</div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}
src/app/components/Testimonials.tsx
import { Star, Quote } from "lucide-react";

export function Testimonials() {
  const testimonials = [
    {
      name: "María González",
      role: "Estudiante de Diseño",
      image: "https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=150&h=150&fit=crop",
      rating: 5,
      text: "¡Increíbles! Las uso para eventos especiales y siempre recibo cumplidos. La calidad es espectacular y duran muchísimo más de lo que esperaba.",
    },
    {
      name: "Laura Martínez",
      role: "Marketing Manager",
      image: "https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=150&h=150&fit=crop",
      rating: 5,
      text: "Perfectas para mi estilo de vida. Las cambio cada semana según mi look. El proceso de personalización es súper intuitivo y divertido.",
    },
    {
      name: "Sofia Ramírez",
      role: "Influencer",
      image: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=150&h=150&fit=crop",
      rating: 5,
      text: "Mis seguidoras siempre me preguntan dónde consigo mis uñas. Nära Nails es mi secreto para tener manicuras impecables sin ir al salón.",
    },
    {
      name: "Ana Torres",
      role: "Emprendedora",
      image: "https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=150&h=150&fit=crop",
      rating: 5,
      text: "Como madre ocupada, estas uñas son un salvavidas. Me toma 5 minutos y tengo una manicura profesional. ¡Y son eco-friendly!",
    },
  ];

  return (
    <section className="py-16 md:py-24" style={{ backgroundColor: '#F5EBE8' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-12">
          <div className="inline-flex items-center gap-2 px-4 py-2 bg-secondary rounded-full mb-4">
            <Star className="w-4 h-4 text-primary fill-current" />
            <span className="text-sm text-primary font-medium">Testimonios Reales</span>
          </div>
          <h2 className="text-3xl md:text-4xl lg:text-5xl font-bold text-foreground mb-4">
            Lo Que Dicen Nuestras Clientas
          </h2>
          <p className="text-lg text-muted-foreground max-w-2xl mx-auto">
            Más de 10,000 mujeres ya confían en Nära Nails para su manicura perfecta.
          </p>
        </div>

        <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
          {testimonials.map((testimonial, index) => (
            <div
              key={index}
              className="bg-white rounded-2xl p-6 shadow-sm hover:shadow-lg transition-all relative"
            >
              <Quote className="w-8 h-8 text-primary/20 absolute top-4 right-4" />

              <div className="flex items-center gap-3 mb-4">
                <img
                  src={testimonial.image}
                  alt={testimonial.name}
                  className="w-12 h-12 rounded-full object-cover ring-2 ring-primary/20"
                />
                <div className="flex-1">
                  <h4 className="font-semibold text-foreground text-sm">{testimonial.name}</h4>
                  <p className="text-xs text-muted-foreground">{testimonial.role}</p>
                </div>
              </div>

              <div className="flex gap-1 mb-3">
                {Array.from({ length: testimonial.rating }).map((_, i) => (
                  <Star key={i} className="w-4 h-4 text-yellow-400 fill-current" />
                ))}
              </div>

              <p className="text-sm text-muted-foreground leading-relaxed">
                "{testimonial.text}"
              </p>
            </div>
          ))}
        </div>

        <div className="mt-12 text-center">
          <div className="inline-flex items-center gap-6 bg-white rounded-full px-8 py-4 shadow-md">
            <div className="text-center">
              <div className="text-2xl font-bold text-primary">4.9/5</div>
              <div className="text-xs text-muted-foreground">Valoración Media</div>
            </div>
            <div className="w-px h-12 bg-border"></div>
            <div className="text-center">
              <div className="text-2xl font-bold text-primary">10,247</div>
              <div className="text-xs text-muted-foreground">Reseñas Verificadas</div>
            </div>
            <div className="w-px h-12 bg-border"></div>
            <div className="text-center">
              <div className="text-2xl font-bold text-primary">98%</div>
              <div className="text-xs text-muted-foreground">Recomendarían</div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}
src/app/components/HowToBuy.tsx
import { MousePointer, Palette, Truck, Star } from "lucide-react";

export function HowToBuy() {
  const whatsappNumber = "3203575433";

  const handleBuyNow = () => {
    const message = "¡Hola! Quiero comprar uñas press-on de Nära Nails 💅";
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
    window.open(url, "_blank");
  };

  const scrollToCollections = () => {
    document.getElementById('colecciones')?.scrollIntoView({ behavior: 'smooth' });
  };
  const steps = [
    {
      icon: MousePointer,
      number: "01",
      title: "Elige tu Colección",
      description:
        "Explora nuestras colecciones exclusivas o crea tu diseño personalizado desde cero. Sin límites para tu creatividad.",
    },
    {
      icon: Palette,
      number: "02",
      title: "Personaliza tu Set",
      description:
        "Selecciona forma, color, largo y acabado. Añade detalles especiales como piedras, arte nail o efectos únicos.",
    },
    {
      icon: Truck,
      number: "03",
      title: "Recibe en Casa",
      description:
        "Envío express en 24-48h. Kit completo con todo lo necesario para una aplicación perfecta y duradera.",
    },
  ];

  return (
    <section id="como-comprar" className="py-16 md:py-24" style={{ backgroundColor: '#E5D7D2' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-12 md:mb-16">
          <div className="inline-flex items-center gap-2 px-4 py-2 bg-secondary rounded-full mb-6">
            <Star className="w-4 h-4 text-primary fill-current" />
            <span className="text-sm text-primary">Proceso Simple</span>
          </div>
          <h2 className="text-3xl md:text-4xl lg:text-5xl font-bold text-foreground mb-4">
            Cómo Comprar en 3 Clics
          </h2>
          <p className="text-lg text-muted-foreground max-w-2xl mx-auto">
            Tu manicura perfecta está a solo 3 pasos. Rápido, fácil y con resultados
            profesionales garantizados.
          </p>
        </div>

        <div className="grid md:grid-cols-3 gap-8 md:gap-12 mb-16">
          {steps.map((step, index) => {
            const Icon = step.icon;
            return (
              <div key={index} className="relative">
                <div className="flex flex-col items-center text-center">
                  <div className="relative mb-6">
                    <div className="w-20 h-20 rounded-full bg-gradient-to-br from-primary to-pink-400 flex items-center justify-center shadow-lg">
                      <Icon className="w-10 h-10 text-white" />
                    </div>
                    <div className="absolute -top-2 -right-2 w-12 h-12 rounded-full bg-secondary flex items-center justify-center border-4 border-white">
                      <span className="text-sm font-bold text-primary">{step.number}</span>
                    </div>
                  </div>
                  <h3 className="text-xl font-semibold text-foreground mb-3">{step.title}</h3>
                  <p className="text-muted-foreground">{step.description}</p>
                </div>
                {index < steps.length - 1 && (
                  <div className="hidden md:block absolute top-10 left-[60%] w-[80%] border-t-2 border-dashed border-pink-200" />
                )}
              </div>
            );
          })}
        </div>

        <div className="bg-gradient-to-br from-primary to-pink-500 rounded-3xl p-8 md:p-12 text-white text-center relative overflow-hidden">
          <div className="absolute inset-0 opacity-10">
            <div className="absolute top-0 left-0 w-64 h-64 bg-white rounded-full blur-3xl" />
            <div className="absolute bottom-0 right-0 w-96 h-96 bg-white rounded-full blur-3xl" />
          </div>
          <div className="relative z-10">
            <h3 className="text-2xl md:text-3xl font-bold mb-4">
              ¿Lista para tu Manicura Perfecta?
            </h3>
            <p className="text-lg mb-8 opacity-95 max-w-2xl mx-auto">
              Únete a miles de clientes satisfechas. Calidad premium, resultados profesionales y
              entrega express. Primera compra con 15% de descuento.
            </p>
            <div className="flex flex-col sm:flex-row gap-4 justify-center">
              <button
                onClick={handleBuyNow}
                className="px-8 py-4 bg-white text-primary rounded-full hover:bg-pink-50 transition-colors font-semibold"
              >
                Comprar Ahora
              </button>
              <button
                onClick={scrollToCollections}
                className="px-8 py-4 border-2 border-white text-white rounded-full hover:bg-white/10 transition-colors font-semibold"
              >
                Ver Catálogo Completo
              </button>
            </div>
            <div className="mt-8 flex items-center justify-center gap-8 text-sm">
              <div className="flex items-center gap-2">
                <Star className="w-5 h-5 fill-current" />
                <span>4.9/5 Valoración</span>
              </div>
              <div className="hidden sm:block w-px h-6 bg-white/30" />
              <div>
                <span className="font-semibold">10,000+</span> Clientes Felices
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}
src/app/components/PaymentShipping.tsx
import { CreditCard, Truck, MapPin, Clock, Package } from "lucide-react";

export function PaymentShipping() {
  return (
    <section className="py-16 md:py-20" style={{ backgroundColor: '#F9F3F0' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid md:grid-cols-2 gap-12">
          <div className="bg-white rounded-3xl p-8 shadow-lg border border-pink-100">
            <div className="flex items-center gap-3 mb-6">
              <div className="w-12 h-12 rounded-xl bg-primary/10 flex items-center justify-center">
                <CreditCard className="w-6 h-6 text-primary" />
              </div>
              <h3 className="text-2xl font-bold text-foreground">Métodos de Pago</h3>
            </div>

            <p className="text-muted-foreground mb-6">
              Paga de forma segura con MercadoPago. Aceptamos todas las tarjetas y métodos de pago disponibles.
            </p>

            <div className="space-y-4">
              <div className="flex items-start gap-3">
                <div className="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center flex-shrink-0 mt-0.5">
                  <span className="text-green-600 text-sm">✓</span>
                </div>
                <div>
                  <h4 className="font-semibold text-foreground mb-1">Tarjetas de Crédito/Débito</h4>
                  <p className="text-sm text-muted-foreground">
                    Visa, Mastercard, American Express. Pago en hasta 12 cuotas sin interés.
                  </p>
                </div>
              </div>

              <div className="flex items-start gap-3">
                <div className="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center flex-shrink-0 mt-0.5">
                  <span className="text-green-600 text-sm">✓</span>
                </div>
                <div>
                  <h4 className="font-semibold text-foreground mb-1">Transferencia Bancaria</h4>
                  <p className="text-sm text-muted-foreground">
                    5% de descuento en transferencias. Confirmación inmediata.
                  </p>
                </div>
              </div>

              <div className="flex items-start gap-3">
                <div className="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center flex-shrink-0 mt-0.5">
                  <span className="text-green-600 text-sm">✓</span>
                </div>
                <div>
                  <h4 className="font-semibold text-foreground mb-1">Pago Contra Entrega</h4>
                  <p className="text-sm text-muted-foreground">
                    Disponible en principales ciudades. Paga en efectivo al recibir tu pedido.
                  </p>
                </div>
              </div>
            </div>

            <div className="mt-6 p-4 bg-primary/5 rounded-xl border border-primary/10">
              <div className="flex items-center gap-2 text-sm">
                <svg className="w-20 h-12" viewBox="0 0 100 40" fill="none">
                  <rect x="2" y="8" width="96" height="24" rx="4" fill="#009EE3"/>
                  <text x="50" y="25" textAnchor="middle" fill="white" fontSize="14" fontWeight="bold">MercadoPago</text>
                </svg>
                <span className="text-xs text-muted-foreground">Procesador de pagos oficial</span>
              </div>
            </div>
          </div>

          <div className="bg-white rounded-3xl p-8 shadow-lg border border-pink-100">
            <div className="flex items-center gap-3 mb-6">
              <div className="w-12 h-12 rounded-xl bg-primary/10 flex items-center justify-center">
                <Truck className="w-6 h-6 text-primary" />
              </div>
              <h3 className="text-2xl font-bold text-foreground">Envíos y Entregas</h3>
            </div>

            <p className="text-muted-foreground mb-6">
              Enviamos a toda España con Interrapidísimo. Tu pedido llegará rápido y seguro a la puerta de tu casa.
            </p>

            <div className="space-y-4">
              <div className="flex items-start gap-3">
                <div className="w-8 h-8 rounded-full bg-primary/10 flex items-center justify-center flex-shrink-0 mt-0.5">
                  <Clock className="w-4 h-4 text-primary" />
                </div>
                <div>
                  <h4 className="font-semibold text-foreground mb-1">Envío Express 24-48h</h4>
                  <p className="text-sm text-muted-foreground">
                    Madrid, Barcelona, Valencia. Recibe tu pedido en 1-2 días hábiles. €4.95
                  </p>
                </div>
              </div>

              <div className="flex items-start gap-3">
                <div className="w-8 h-8 rounded-full bg-primary/10 flex items-center justify-center flex-shrink-0 mt-0.5">
                  <MapPin className="w-4 h-4 text-primary" />
                </div>
                <div>
                  <h4 className="font-semibold text-foreground mb-1">Envío Estándar 3-5 días</h4>
                  <p className="text-sm text-muted-foreground">
                    Resto de España peninsular. Entrega garantizada. €2.95
                  </p>
                </div>
              </div>

              <div className="flex items-start gap-3">
                <div className="w-8 h-8 rounded-full bg-primary/10 flex items-center justify-center flex-shrink-0 mt-0.5">
                  <Package className="w-4 h-4 text-primary" />
                </div>
                <div>
                  <h4 className="font-semibold text-foreground mb-1">Envío GRATIS</h4>
                  <p className="text-sm text-muted-foreground">
                    En compras superiores a €40. Aplicable a toda España.
                  </p>
                </div>
              </div>
            </div>

            <div className="mt-6 p-4 bg-gradient-to-r from-primary/10 to-pink-100/50 rounded-xl border border-primary/20">
              <h4 className="font-semibold text-foreground mb-2">Seguimiento en Tiempo Real</h4>
              <p className="text-sm text-muted-foreground">
                Recibe un código de seguimiento por email y SMS para rastrear tu pedido en cada paso del camino.
              </p>
            </div>

            <div className="mt-4 flex items-center gap-3">
              <div className="px-4 py-2 bg-orange-100 rounded-lg">
                <span className="text-orange-700 font-semibold text-xs">Interrapidísimo</span>
              </div>
              <div className="text-xs text-muted-foreground">Courier oficial</div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}
📱 COMPONENTES - Parte 4 (Final)
src/app/components/FAQ.tsx
import { Plus, Minus } from "lucide-react";
import { useState } from "react";

export function FAQ() {
  const [openIndex, setOpenIndex] = useState<number | null>(0);
  const whatsappNumber = "3203575433";

  const handleContactSupport = () => {
    const message = "¡Hola! Necesito ayuda con información sobre Nära Nails 💅";
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
    window.open(url, "_blank");
  };

  const faqs = [
    {
      question: "¿Cuánto duran las uñas press-on?",
      answer: "Con el cuidado adecuado, nuestras uñas press-on pueden durar entre 1-2 semanas. Son reutilizables, así que puedes usarlas múltiples veces si las cuidas correctamente."
    },
    {
      question: "¿Cómo aplico las uñas press-on?",
      answer: "Es súper fácil: 1) Limpia tus uñas naturales, 2) Elige el tamaño correcto para cada dedo, 3) Aplica el adhesivo incluido, 4) Presiona firmemente durante 30 segundos. ¡Listo en 5 minutos!"
    },
    {
      question: "¿Puedo personalizar completamente mis uñas?",
      answer: "¡Absolutamente! Puedes elegir forma (ovalada, cuadrada, almendrada, stiletto), largo (corta, media, larga), color, acabado (mate, brillante, cromado) y añadir diseños personalizados, piedras o arte nail."
    },
    {
      question: "¿Dañan las uñas naturales?",
      answer: "No. A diferencia del gel o acrílico, nuestras uñas press-on no requieren limado agresivo ni químicos que debiliten tus uñas naturales. De hecho, protegen tus uñas mientras las usas."
    },
    {
      question: "¿Qué incluye cada set?",
      answer: "Cada set incluye 10 uñas press-on premium (una para cada dedo), adhesivos premium de larga duración, una lima profesional y una guía detallada de aplicación paso a paso."
    },
    {
      question: "¿Puedo quitarlas fácilmente?",
      answer: "Sí, son muy fáciles de remover. Sumerge tus manos en agua tibia con jabón por 10-15 minutos y despega suavemente desde los laterales. Sin dolor, sin daño."
    },
    {
      question: "¿Ofrecen envío internacional?",
      answer: "Actualmente enviamos a toda España con Interrapidísimo. Estamos trabajando para expandir nuestros envíos internacionales próximamente. ¡Suscríbete al newsletter para ser la primera en saberlo!"
    },
    {
      question: "¿Tienen política de devolución?",
      answer: "Sí, ofrecemos 30 días de garantía. Si no estás completamente satisfecha con tu compra, puedes devolverla para reembolso completo. Tu satisfacción es nuestra prioridad."
    }
  ];

  return (
    <section className="py-16 md:py-24" style={{ backgroundColor: '#E8D5D0' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center mb-12">
          <h2 className="text-3xl md:text-4xl lg:text-5xl font-bold text-foreground mb-4">
            Preguntas Frecuentes
          </h2>
          <p className="text-lg text-muted-foreground max-w-2xl mx-auto">
            Todo lo que necesitas saber sobre Nära Nails. ¿No encuentras tu respuesta? ¡Contáctanos!
          </p>
        </div>

        <div className="max-w-3xl mx-auto space-y-4">
          {faqs.map((faq, index) => (
            <div
              key={index}
              className="bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow overflow-hidden"
            >
              <button
                onClick={() => setOpenIndex(openIndex === index ? null : index)}
                className="w-full px-6 py-5 flex items-center justify-between text-left hover:bg-pink-50/50 transition-colors"
              >
                <span className="font-semibold text-foreground pr-4">{faq.question}</span>
                {openIndex === index ? (
                  <Minus className="w-5 h-5 text-primary flex-shrink-0" />
                ) : (
                  <Plus className="w-5 h-5 text-primary flex-shrink-0" />
                )}
              </button>
              {openIndex === index && (
                <div className="px-6 pb-5 text-muted-foreground animate-in slide-in-from-top-2">
                  {faq.answer}
                </div>
              )}
            </div>
          ))}
        </div>

        <div className="mt-12 text-center">
          <p className="text-muted-foreground mb-4">
            ¿Tienes más preguntas? Estamos aquí para ayudarte
          </p>
          <div className="flex flex-col sm:flex-row gap-4 justify-center">
            <button
              onClick={handleContactSupport}
              className="px-6 py-3 bg-primary text-white rounded-full hover:bg-pink-600 transition-colors"
            >
              Contactar Soporte
            </button>
            <button
              onClick={handleContactSupport}
              className="px-6 py-3 border-2 border-primary text-primary rounded-full hover:bg-secondary transition-colors"
            >
              Ver Guía Completa
            </button>
          </div>
        </div>
      </div>
    </section>
  );
}
src/app/components/Newsletter.tsx
import { Mail, Gift, Sparkles } from "lucide-react";
import { useState } from "react";

export function Newsletter() {
  const [email, setEmail] = useState("");
  const [subscribed, setSubscribed] = useState(false);

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (email) {
      // Aquí iría la integración con el servicio de email marketing
      setSubscribed(true);
      setTimeout(() => {
        setSubscribed(false);
        setEmail("");
      }, 5000);
    }
  };

  return (
    <section className="py-16 md:py-20" style={{ backgroundColor: '#D4B5AB' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8">
        <div className="max-w-4xl mx-auto">
          <div className="rounded-3xl p-8 md:p-12 text-white relative overflow-hidden" style={{ background: 'linear-gradient(to right, #C7998E, #B8897C, #C7B0A6)' }}>
            <div className="absolute top-0 right-0 w-64 h-64 bg-white/10 rounded-full blur-3xl -mr-32 -mt-32"></div>
            <div className="absolute bottom-0 left-0 w-96 h-96 bg-white/10 rounded-full blur-3xl -ml-48 -mb-48"></div>

            <div className="relative z-10 text-center">
              <div className="inline-flex items-center gap-2 px-4 py-2 bg-white/20 rounded-full mb-6">
                <Gift className="w-5 h-5" />
                <span className="font-semibold">¡15% de descuento exclusivo!</span>
              </div>

              <h2 className="text-3xl md:text-4xl font-bold mb-4">
                Únete a la Comunidad Nära
              </h2>
              <p className="text-lg mb-8 opacity-95 max-w-2xl mx-auto">
                Suscríbete y recibe 15% de descuento en tu primera compra, acceso anticipado a nuevas colecciones y tips exclusivos de nail art.
              </p>

              {!subscribed ? (
                <form onSubmit={handleSubmit} className="max-w-md mx-auto">
                  <div className="flex gap-3">
                    <div className="flex-1 relative">
                      <Mail className="absolute left-4 top-1/2 -translate-y-1/2 w-5 h-5 text-muted-foreground" />
                      <input
                        type="email"
                        value={email}
                        onChange={(e) => setEmail(e.target.value)}
                        placeholder="tu@email.com"
                        required
                        className="w-full pl-12 pr-4 py-4 rounded-full border-2 border-white/30 bg-white/90 backdrop-blur focus:outline-none focus:border-white text-foreground placeholder:text-muted-foreground"
                      />
                    </div>
                    <button
                      type="submit"
                      className="px-8 py-4 bg-white text-primary rounded-full hover:bg-pink-50 transition-colors font-semibold whitespace-nowrap"
                    >
                      Suscribirme
                    </button>
                  </div>
                  <p className="text-xs mt-4 opacity-80">
                    Al suscribirte aceptas recibir emails promocionales. Puedes darte de baja en cualquier momento.
                  </p>
                </form>
              ) : (
                <div className="max-w-md mx-auto bg-white/20 backdrop-blur rounded-2xl p-6 animate-in fade-in slide-in-from-bottom-4">
                  <div className="flex items-center justify-center gap-3 mb-3">
                    <Sparkles className="w-6 h-6" />
                    <span className="text-xl font-semibold">¡Bienvenida a Nära!</span>
                  </div>
                  <p className="text-sm opacity-90">
                    Revisa tu email para obtener tu código de descuento del 15% 💅✨
                  </p>
                </div>
              )}

              <div className="mt-10 flex flex-wrap justify-center gap-8 text-sm">
                <div className="flex items-center gap-2">
                  <div className="w-8 h-8 rounded-full bg-white/20 flex items-center justify-center">
                    <span className="text-lg">💌</span>
                  </div>
                  <span>Ofertas exclusivas</span>
                </div>
                <div className="flex items-center gap-2">
                  <div className="w-8 h-8 rounded-full bg-white/20 flex items-center justify-center">
                    <span className="text-lg">✨</span>
                  </div>
                  <span>Nuevas colecciones</span>
                </div>
                <div className="flex items-center gap-2">
                  <div className="w-8 h-8 rounded-full bg-white/20 flex items-center justify-center">
                    <span className="text-lg">💅</span>
                  </div>
                  <span>Tips de nail art</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
}
src/app/components/Footer.tsx
import { Sparkles, Instagram, Facebook, Mail, Phone, Shield, Lock, Award } from "lucide-react";
import { useState } from "react";

export function Footer() {
  const [newsletterEmail, setNewsletterEmail] = useState("");
  const whatsappNumber = "3203575433";

  const handleNewsletterSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (newsletterEmail) {
      const message = `¡Hola! Quiero suscribirme al newsletter de Nära Nails con el email: ${newsletterEmail}`;
      const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
      window.open(url, "_blank");
      setNewsletterEmail("");
    }
  };

  const handleSocialClick = (platform: string) => {
    alert(`Próximamente podrás seguirnos en ${platform}! 🎉`);
  };
  return (
    <footer className="bg-gradient-to-b border-t" style={{ backgroundColor: '#F9F3F0', borderColor: '#E8D5D0' }}>
      <div className="container mx-auto px-4 sm:px-6 lg:px-8 py-12 md:py-16">
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-12">
          <div>
            <div className="flex items-center gap-2 mb-4">
              <Sparkles className="w-6 h-6 text-primary" />
              <span className="font-semibold text-xl text-primary">Nära Nails</span>
            </div>
            <p className="text-sm text-muted-foreground mb-6">
              Uñas press-on personalizadas de calidad premium. Belleza profesional en minutos.
            </p>
            <div className="flex gap-4">
              <button
                onClick={() => handleSocialClick('Instagram')}
                className="w-10 h-10 rounded-full bg-secondary hover:bg-primary hover:text-white transition-colors flex items-center justify-center"
              >
                <Instagram className="w-5 h-5" />
              </button>
              <button
                onClick={() => handleSocialClick('Facebook')}
                className="w-10 h-10 rounded-full bg-secondary hover:bg-primary hover:text-white transition-colors flex items-center justify-center"
              >
                <Facebook className="w-5 h-5" />
              </button>
              <a href="mailto:hola@naranails.com">
                <button className="w-10 h-10 rounded-full bg-secondary hover:bg-primary hover:text-white transition-colors flex items-center justify-center">
                  <Mail className="w-5 h-5" />
                </button>
              </a>
            </div>
          </div>

          <div>
            <h3 className="font-semibold text-foreground mb-4">Tienda</h3>
            <ul className="space-y-3 text-sm">
              <li>
                <a href="#colecciones" className="text-muted-foreground hover:text-primary transition-colors">
                  Colecciones
                </a>
              </li>
              <li>
                <a href="#personaliza" className="text-muted-foreground hover:text-primary transition-colors">
                  Personalizar
                </a>
              </li>
              <li>
                <a href="#colecciones" className="text-muted-foreground hover:text-primary transition-colors">
                  Nuevos Lanzamientos
                </a>
              </li>
              <li>
                <a href="#colecciones" className="text-muted-foreground hover:text-primary transition-colors">
                  Best Sellers
                </a>
              </li>
            </ul>
          </div>

          <div>
            <h3 className="font-semibold text-foreground mb-4">Ayuda</h3>
            <ul className="space-y-3 text-sm">
              <li>
                <a href={`https://wa.me/${whatsappNumber}?text=${encodeURIComponent('Hola, necesito ayuda con la guía de aplicación')}`} target="_blank" rel="noopener noreferrer" className="text-muted-foreground hover:text-primary transition-colors">
                  Guía de Aplicación
                </a>
              </li>
              <li>
                <a href="#como-comprar" className="text-muted-foreground hover:text-primary transition-colors">
                  Envíos y Devoluciones
                </a>
              </li>
              <li>
                <a href="#" className="text-muted-foreground hover:text-primary transition-colors">
                  Preguntas Frecuentes
                </a>
              </li>
              <li>
                <a href={`https://wa.me/${whatsappNumber}`} target="_blank" rel="noopener noreferrer" className="text-muted-foreground hover:text-primary transition-colors">
                  Contacto
                </a>
              </li>
            </ul>
          </div>

          <div>
            <h3 className="font-semibold text-foreground mb-4">Contacto</h3>
            <div className="space-y-3 text-sm">
              <a href="mailto:hola@naranails.com" className="flex items-center gap-3 text-muted-foreground hover:text-primary transition-colors">
                <Mail className="w-4 h-4 text-primary flex-shrink-0" />
                <span>hola@naranails.com</span>
              </a>
              <a href={`https://wa.me/${whatsappNumber}`} target="_blank" rel="noopener noreferrer" className="flex items-center gap-3 text-muted-foreground hover:text-primary transition-colors">
                <Phone className="w-4 h-4 text-primary flex-shrink-0" />
                <span>+57 320 357 5433</span>
              </a>
              <div className="mt-6">
                <p className="text-xs text-muted-foreground mb-2">
                  Suscríbete a nuestro newsletter
                </p>
                <form onSubmit={handleNewsletterSubmit} className="flex gap-2">
                  <input
                    type="email"
                    value={newsletterEmail}
                    onChange={(e) => setNewsletterEmail(e.target.value)}
                    placeholder="tu@email.com"
                    required
                    className="flex-1 px-4 py-2 rounded-full border border-pink-200 focus:outline-none focus:border-primary text-sm"
                  />
                  <button
                    type="submit"
                    className="px-4 py-2 bg-primary text-white rounded-full hover:bg-pink-600 transition-colors text-sm"
                  >
                    OK
                  </button>
                </form>
              </div>
            </div>
          </div>
        </div>

        <div className="border-t border-pink-200 pt-8">
          <div className="flex flex-wrap justify-center gap-6 mb-6">
            <div className="flex items-center gap-2 text-xs text-muted-foreground">
              <Shield className="w-4 h-4 text-green-600" />
              <span>SSL Seguro</span>
            </div>
            <div className="flex items-center gap-2 text-xs text-muted-foreground">
              <Lock className="w-4 h-4 text-blue-600" />
              <span>Pago Protegido</span>
            </div>
            <div className="flex items-center gap-2 text-xs text-muted-foreground">
              <Award className="w-4 h-4 text-purple-600" />
              <span>Certificado ISO 9001</span>
            </div>
            <div className="flex items-center gap-2 text-xs text-muted-foreground">
              <span className="text-green-600 font-semibold">✓</span>
              <span>100% Eco-Friendly</span>
            </div>
          </div>

          <div className="flex flex-col md:flex-row justify-between items-center gap-4 text-sm text-muted-foreground">
            <p>© 2026 Nära Nails. Todos los derechos reservados.</p>
            <div className="flex gap-6">
              <a href="#" className="hover:text-primary transition-colors">
                Política de Privacidad
              </a>
              <a href="#" className="hover:text-primary transition-colors">
                Términos y Condiciones
              </a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  );
}
src/app/components/WhatsAppButton.tsx
import { useState } from "react";

const WhatsAppIcon = () => (
  <svg
    viewBox="0 0 32 32"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    className="w-8 h-8 md:w-9 md:h-9"
  >
    <path
      fillRule="evenodd"
      clipRule="evenodd"
      d="M16 31C23.732 31 30 24.732 30 17C30 9.26801 23.732 3 16 3C8.26801 3 2 9.26801 2 17C2 19.5109 2.661 21.8674 3.81847 23.905L2 31L9.31486 29.3038C11.3014 30.3854 13.5789 31 16 31Z"
      fill="white"
    />
    <path
      d="M12.5 9.49989C12.1672 8.83131 11.6565 8.8905 11.1407 8.8905C10.2188 8.8905 8.78125 9.99478 8.78125 12.05C8.78125 13.7343 9.52345 15.578 12.0244 18.3361C14.438 20.9979 17.6094 22.3748 20.2422 22.3279C22.875 22.2811 23.4167 20.0154 23.4167 19.2503C23.4167 18.9112 23.2062 18.742 23.0613 18.696C22.1641 18.2654 20.5093 17.4631 20.1328 17.3124C19.7563 17.1617 19.5597 17.3656 19.4375 17.4765C19.0961 17.8018 18.4193 18.7608 18.1875 18.9765C17.9558 19.1922 17.6103 19.083 17.4665 19.0015C16.9374 18.7892 15.5029 18.1511 14.3595 17.0426C12.9453 15.6718 12.8623 15.2001 12.5959 14.7803C12.3828 14.4444 12.5392 14.2384 12.6172 14.1483C12.9219 13.7968 13.3426 13.254 13.5313 12.9843C13.7199 12.7145 13.5702 12.305 13.4803 12.05C13.0938 10.953 12.7663 10.0347 12.5 9.49989Z"
      fill="#25D366"
    />
  </svg>
);

export function WhatsAppButton() {
  const [showTooltip, setShowTooltip] = useState(false);
  const whatsappNumber = "3203575433";
  const message = "¡Hola! Me interesan las uñas press-on de Nära Nails 💅";

  const handleClick = () => {
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
    window.open(url, "_blank");
  };

  return (
    <>
      <button
        onClick={handleClick}
        onMouseEnter={() => setShowTooltip(true)}
        onMouseLeave={() => setShowTooltip(false)}
        className="fixed bottom-6 right-6 z-50 w-14 h-14 md:w-16 md:h-16 rounded-full shadow-lg hover:shadow-xl transition-all flex items-center justify-center group animate-bounce hover:animate-none"
        style={{ backgroundColor: '#25D366' }}
        aria-label="Chat con WhatsApp"
      >
        <WhatsAppIcon />
        <span className="absolute -top-1 -right-1 w-4 h-4 bg-red-500 rounded-full animate-pulse"></span>
      </button>

      {showTooltip && (
        <div className="fixed bottom-24 right-6 z-50 bg-white rounded-2xl shadow-xl p-4 max-w-xs animate-in slide-in-from-bottom-2">
          <div className="flex items-start gap-3">
            <div className="w-10 h-10 rounded-full flex items-center justify-center flex-shrink-0" style={{ backgroundColor: '#25D366' }}>
              <svg
                viewBox="0 0 24 24"
                fill="white"
                className="w-6 h-6"
              >
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
              </svg>
            </div>
            <div className="flex-1">
              <p className="font-semibold text-sm" style={{ color: '#6B5448' }}>
                ¿Necesitas ayuda?
              </p>
              <p className="text-xs" style={{ color: '#8B7367' }}>
                Chatea con nosotras por WhatsApp. ¡Respondemos en minutos!
              </p>
            </div>
          </div>
        </div>
      )}
    </>
  );
}
src/app/components/Chatbot.tsx
import { MessageCircle, X, Send, Sparkles } from "lucide-react";
import { useState } from "react";

export function Chatbot() {
  const [isOpen, setIsOpen] = useState(false);
  const [messages, setMessages] = useState([
    {
      type: "bot",
      text: "¡Hola! 👋 Soy el asistente virtual de Nära Nails. ¿En qué puedo ayudarte hoy?",
      time: new Date().toLocaleTimeString("es-ES", { hour: "2-digit", minute: "2-digit" })
    }
  ]);
  const [inputValue, setInputValue] = useState("");

  const quickReplies = [
    "Ver colecciones",
    "¿Cómo personalizar?",
    "Tiempos de envío",
    "Métodos de pago"
  ];

  const handleQuickReply = (reply: string) => {
    handleSendMessage(reply);
  };

  const handleSendMessage = (text?: string) => {
    const messageText = text || inputValue.trim();
    if (!messageText) return;

    const userMessage = {
      type: "user",
      text: messageText,
      time: new Date().toLocaleTimeString("es-ES", { hour: "2-digit", minute: "2-digit" })
    };

    setMessages(prev => [...prev, userMessage]);
    setInputValue("");

    setTimeout(() => {
      let botResponse = "";
      const lowerText = messageText.toLowerCase();

      if (lowerText.includes("coleccion") || lowerText.includes("diseño")) {
        botResponse = "Tenemos 6 colecciones exclusivas: Romance Rosa, Elegancia Natural, Glamour Pink y más. ¿Te gustaría ver alguna en particular? 💅";
      } else if (lowerText.includes("personalizar") || lowerText.includes("custom")) {
        botResponse = "¡Personalizar es fácil! 1️⃣ Elige forma y largo 2️⃣ Selecciona color y acabado 3️⃣ Añade diseños especiales. ¿Te ayudo a empezar?";
      } else if (lowerText.includes("envío") || lowerText.includes("entrega")) {
        botResponse = "Enviamos con Interrapidísimo 📦 Express 24-48h (€4.95) o Estándar 3-5 días (€2.95). ¡Envío GRATIS en compras +€40!";
      } else if (lowerText.includes("pago") || lowerText.includes("pagar")) {
        botResponse = "Aceptamos tarjetas, transferencia (5% dto) y pago contra entrega 💳 Procesado de forma segura con MercadoPago. ¿Alguna duda específica?";
      } else if (lowerText.includes("precio") || lowerText.includes("costo")) {
        botResponse = "Nuestros sets desde €24.90 incluyen 24 uñas, adhesivos premium, lima y guía. ¡Primera compra con 15% descuento! 🎉";
      } else if (lowerText.includes("hola") || lowerText.includes("hi")) {
        botResponse = "¡Hola! 😊 Estoy aquí para ayudarte con cualquier duda sobre nuestras uñas press-on. ¿Qué te gustaría saber?";
      } else {
        botResponse = "Entiendo tu consulta. ¿Puedo ayudarte con información sobre colecciones, personalización, envíos o métodos de pago? También puedes contactarnos por WhatsApp para atención personalizada. 💬";
      }

      const botMessage = {
        type: "bot",
        text: botResponse,
        time: new Date().toLocaleTimeString("es-ES", { hour: "2-digit", minute: "2-digit" })
      };

      setMessages(prev => [...prev, botMessage]);
    }, 800);
  };

  return (
    <>
      {!isOpen && (
        <button
          onClick={() => setIsOpen(true)}
          className="fixed bottom-24 right-6 z-40 w-14 h-14 md:w-16 md:h-16 text-white rounded-full shadow-lg hover:shadow-xl transition-all flex items-center justify-center group"
          style={{ backgroundColor: '#C7998E' }}
          aria-label="Abrir chat"
        >
          <Sparkles className="w-7 h-7 md:w-8 md:h-8" />
        </button>
      )}

      {isOpen && (
        <div className="fixed bottom-6 right-6 z-40 w-[350px] md:w-[400px] h-[500px] bg-white rounded-3xl shadow-2xl flex flex-col animate-in slide-in-from-bottom-4">
          <div className="text-white p-4 rounded-t-3xl flex items-center justify-between" style={{ background: 'linear-gradient(to right, #C7998E, #B8897C)' }}>
            <div className="flex items-center gap-3">
              <div className="w-10 h-10 rounded-full bg-white/20 flex items-center justify-center">
                <Sparkles className="w-5 h-5" />
              </div>
              <div>
                <h3 className="font-semibold">Asistente Nära</h3>
                <p className="text-xs opacity-90">Online - Responde en segundos</p>
              </div>
            </div>
            <button
              onClick={() => setIsOpen(false)}
              className="w-8 h-8 rounded-full hover:bg-white/20 flex items-center justify-center transition-colors"
            >
              <X className="w-5 h-5" />
            </button>
          </div>

          <div className="flex-1 overflow-y-auto p-4 space-y-3">
            {messages.map((message, index) => (
              <div
                key={index}
                className={`flex ${message.type === "user" ? "justify-end" : "justify-start"}`}
              >
                <div
                  className={`max-w-[75%] rounded-2xl px-4 py-2.5 ${
                    message.type === "user"
                      ? "text-white rounded-br-md"
                      : "bg-gray-100 rounded-bl-md"
                  }`}
                  style={message.type === "user" ? { backgroundColor: '#C7998E', color: '#ffffff' } : { color: '#6B5448' }}
                >
                  <p className="text-sm">{message.text}</p>
                  <p
                    className={`text-xs mt-1 ${
                      message.type === "user" ? "text-white/70" : "text-muted-foreground"
                    }`}
                  >
                    {message.time}
                  </p>
                </div>
              </div>
            ))}
          </div>

          {messages.length === 1 && (
            <div className="px-4 pb-3">
              <p className="text-xs text-muted-foreground mb-2">Respuestas rápidas:</p>
              <div className="flex flex-wrap gap-2">
                {quickReplies.map((reply, index) => (
                  <button
                    key={index}
                    onClick={() => handleQuickReply(reply)}
                    className="px-3 py-1.5 text-sm rounded-full transition-colors hover:text-white"
                    style={{ backgroundColor: '#E8D5D0', color: '#6B5448' }}
                    onMouseEnter={(e) => e.currentTarget.style.backgroundColor = '#C7998E'}
                    onMouseLeave={(e) => e.currentTarget.style.backgroundColor = '#E8D5D0'}
                  >
                    {reply}
                  </button>
                ))}
              </div>
            </div>
          )}

          <div className="p-4 border-t border-gray-100">
            <div className="flex gap-2">
              <input
                type="text"
                value={inputValue}
                onChange={(e) => setInputValue(e.target.value)}
                onKeyPress={(e) => e.key === "Enter" && handleSendMessage()}
                placeholder="Escribe tu mensaje..."
                className="flex-1 px-4 py-2.5 border rounded-full focus:outline-none text-sm"
                style={{ borderColor: '#E8D5D0', color: '#6B5448' }}
              />
              <button
                onClick={() => handleSendMessage()}
                className="w-10 h-10 text-white rounded-full flex items-center justify-center transition-colors flex-shrink-0"
                style={{ backgroundColor: '#C7998E' }}
              >
                <Send className="w-4 h-4" />
              </button>
            </div>
          </div>
        </div>
      )}
    </>
  );
}
src/app/components/Analytics.tsx
import { useEffect } from "react";

declare global {
  interface Window {
    gtag?: (...args: any[]) => void;
    dataLayer?: any[];
  }
}

export function Analytics() {
  useEffect(() => {
    // Google Analytics 4 - Placeholder
    // En producción, reemplaza 'G-XXXXXXXXXX' con tu ID real de Google Analytics
    const GA_MEASUREMENT_ID = "G-XXXXXXXXXX";

    // Crear script de Google Analytics
    const script1 = document.createElement("script");
    script1.async = true;
    script1.src = `https://www.googletagmanager.com/gtag/js?id=${GA_MEASUREMENT_ID}`;
    document.head.appendChild(script1);

    // Configurar Google Analytics
    const script2 = document.createElement("script");
    script2.innerHTML = `
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', '${GA_MEASUREMENT_ID}', {
        page_path: window.location.pathname,
      });
    `;
    document.head.appendChild(script2);

    // Configurar Facebook Pixel - Placeholder
    const FB_PIXEL_ID = "YOUR_PIXEL_ID";
    const script3 = document.createElement("script");
    script3.innerHTML = `
      !function(f,b,e,v,n,t,s)
      {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
      n.callMethod.apply(n,arguments):n.queue.push(arguments)};
      if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
      n.queue=[];t=b.createElement(e);t.async=!0;
      t.src=v;s=b.getElementsByTagName(e)[0];
      s.parentNode.insertBefore(t,s)}(window, document,'script',
      'https://connect.facebook.net/en_US/fbevents.js');
      fbq('init', '${FB_PIXEL_ID}');
      fbq('track', 'PageView');
    `;
    document.head.appendChild(script3);

    // Limpiar scripts al desmontar
    return () => {
      document.head.removeChild(script1);
      document.head.removeChild(script2);
      document.head.removeChild(script3);
    };
  }, []);

  return null;
}

// Hook para tracking de eventos
export function useAnalytics() {
  const trackEvent = (eventName: string, params?: Record<string, any>) => {
    if (typeof window.gtag !== "undefined") {
      window.gtag("event", eventName, params);
    }
  };

  const trackPageView = (pagePath: string) => {
    if (typeof window.gtag !== "undefined") {
      window.gtag("config", "G-XXXXXXXXXX", {
        page_path: pagePath,
      });
    }
  };

  const trackPurchase = (value: number, currency: string = "EUR") => {
    if (typeof window.gtag !== "undefined") {
      window.gtag("event", "purchase", {
        value: value,
        currency: currency,
      });
    }
  };

  const trackAddToCart = (productName: string, value: number) => {
    if (typeof window.gtag !== "undefined") {
      window.gtag("event", "add_to_cart", {
        items: [
          {
            name: productName,
            value: value,
          },
        ],
      });
    }
  };

  return {
    trackEvent,
    trackPageView,
    trackPurchase,
    trackAddToCart,
  };
}

