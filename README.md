{
  "name": "cholilah-lenirra",
  "version": "1.0.0",
  "private": true,
  "homepage": "https://<your-github-username>.github.io/cholilah-lenirra",
  "dependencies": {
    "framer-motion": "^10.12.5",
    "lucide-react": "^0.275.0",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-scripts": "5.0.1"
  },
  "devDependencies": {
    "gh-pages": "^5.0.0"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  }
}
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {
      fontFamily: {
        poppins: ['Poppins', 'sans-serif'],
        fredoka: ['Fredoka One', 'cursive']
      },
      colors: {
        dusty: '#C99A9A',
        sage: '#A9B9A1',
        beige: '#E8DCC0',
        skyblue: '#AFCAD9',
        cream: '#F5F4EE'
      }
    },
  },
  plugins: [],
}
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&family=Fredoka+One&display=swap');

@tailwind base;
@tailwind components;
@tailwind utilities;

/* handwriting style fallback (for quotes) */
@layer components {
  .font-handwritten {
    font-family: 'Fredoka One', 'Poppins', sans-serif;
  }
}

/* soft paper texture overlay */
.site-overlay {
  background: linear-gradient(180deg, rgba(245,244,238,0.85), rgba(245,244,238,0.85));
}

/* gentle rounded cards */
.glass-card {
  background: rgba(255,255,255,0.85);
  backdrop-filter: blur(4px);
  border-radius: 16px;
  box-shadow: 0 6px 24px rgba(15, 23, 42, 0.08);
}

/* small sticker/doodle style */
.sticker {
  transform: rotate(-6deg);
  font-weight: 700;
  padding: 6px 10px;
  border-radius: 10px;
  background: rgba(255,255,255,0.9);
}

/* color chips */
.color-chip {
  width: 96px;
  height: 72px;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 8px;
  color: #111827;
}

/* section full-screen min height */
.section-min {
  min-height: 72vh;
}

/* subtle section divider */
.section-divider {
  height: 1px;
  background: rgba(0,0,0,0.06);
  margin: 28px 0;
}

/* responsive tweaks */
@media (min-width: 768px) {
  .title-xl { font-size: 2.75rem; }
}
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
import React from 'react';
import { motion } from 'framer-motion';
import { Camera, Mountain, Heart, Sun } from 'lucide-react';
import Header from './components/Header';
import Footer from './components/Footer';

const SECTIONS = [
  {
    id: 'cover',
    title: 'The Cholilah Goes to Lenirra',
    subtitle: 'A Family Staycation Guidebook • Lenirra Glamping, Cijeruk, Kabupaten Bogor • 6–7 December 2025',
    mini: '“Fun, laughter, and a whole lot of memories — here we go!”',
    bg: 'https://images.unsplash.com/photo-1501785888041-af3ef285b470?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=3a5d85fdb23b7b8b98cd7a9f4b6c9beb'
  },
  {
    id: 'welcome',
    title: 'Welcome to Our Staycation!',
    text: `Hey Cholilah Fam! We’re heading to Lenirra Glamping — a nature-packed getaway filled with sawah views, mountain air, and family fun. We’ll arrive around 11 AM, so even before check-in, let’s explore!`,
    activities: ['Walk around the sawah', 'Enjoy the mountain view', 'Jump in the pool', 'Ride the ATV', 'Go biking', 'Eat at the cozy resto'],
    bg: 'https://images.unsplash.com/photo-1521295121783-8a321d551ad2?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=7b7f7f3a6e33a9cea5bdb0f09a6f5c3e'
  },
  {
    id: 'palette',
    title: "Let's Coordinate!",
    colors: [
      {label: 'Dusty Rose', hex: '#C99A9A', vibe: 'Warm & soft'},
      {label: 'Sage Green', hex: '#A9B9A1', vibe: 'Calm & natural'},
      {label: 'Beige', hex: '#E8DCC0', vibe: 'Neutral & classic'},
      {label: 'Sky Blue', hex: '#AFCAD9', vibe: 'Fresh & airy'},
      {label: 'Cream White', hex: '#F5F4EE', vibe: 'Bright & clean'}
    ],
    bg: 'https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=bb2ce97f984a0a0aa1b64a0b2b9d7d01'
  },
  {
    id: 'photoshoot',
    title: 'Ready, Set, Smile!',
    subtitle: 'Photoshoot Day Plan',
    rows: [
      '📅 Photoshoot: 7 December (before check-out)',
      '⏰ Duration: 3–4 hours',
      '📸 1 photographer for all families',
      '👕 Whoever’s ready first, go first!',
      'Tip: Wear your coordinated colors & bring small props (hats, baskets, sunnies, scarves).'
    ],
    bg: 'https://images.unsplash.com/photo-1519681393784-d120267933ba?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=5b7af997f0b2d4a0e9b3b19fdb6efb12'
  },
  {
    id: 'pose-big',
    title: 'Pose Inspo: The Big Family',
    text: [
      'Everyone waving (like a movie poster)',
      'Mix standing & sitting layers',
      'Kids in front, grandparents in middle',
      'Laughing candidly',
      '“Lenirraaa!” shout for the last shot'
    ],
    bg: 'https://images.unsplash.com/photo-1520975682074-6fe3320b3f2d?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=3f2f41b6cbbf3d7fe4c6d4f0c3e6f9b9'
  },
  {
    id: 'pose-little',
    title: 'Pose Inspo: Little Family',
    text: [
      'Sit on a picnic mat with kids on laps',
      'Grandparents holding hands with grandkids',
      'Hug line from behind',
      'Walk together in sawah path',
      'Generational lineup shot'
    ],
    bg: 'https://images.unsplash.com/photo-1542744173-8e7e53415bb0?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=8a3e0ea0b5f8d2e7a4a3f2a5e3fb2c6a'
  },
  {
    id: 'pose-2kids',
    title: 'Pose Inspo: Parents + 2 Kids',
    text: [
      'Walking toward camera hand-in-hand',
      'Piggyback moment',
      'Sitting on grass laughing',
      'Family group hug',
      'Kids running forward with parents behind'
    ],
    bg: 'https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=7e1f1a3c8c9f4b2d34b0d9a2c3f9e2b5'
  },
  {
    id: 'pose-1kid',
    title: 'Pose Inspo: Parents + 1 Kid',
    text: [
      'Swing kid mid-air by both hands',
      'Sit on grass, kid standing in middle',
      'Kid pointing at view',
      'Soft cuddle pose'
    ],
    bg: 'https://images.unsplash.com/photo-1469474968028-56623f02e42e?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=eae0c6e7c7b2f0c8c2a9c3f6a9d1b2c7'
  },
  {
    id: 'pose-baby',
    title: 'Pose Inspo: Parents + Baby',
    text: [
      'Baby on lap',
      'Parents kissing baby',
      'Hold baby up gently (Lion King moment!)',
      'Close-up hands or feet',
      'Lying down on blanket together'
    ],
    bg: 'https://images.unsplash.com/photo-1514888286974-6c03e2ca1dba?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=2ed5b4b9d1a7a9a5c6b6f7f2e6b3d5f2'
  },
  {
    id: 'bonus',
    title: "Don't Miss These Moments!",
    text: [
      'Kids jumping into the pool',
      'Siblings laughing on bikes',
      'Family cheers at the resto',
      'Drone shot of full family',
      'Golden hour silhouette'
    ],
    bg: 'https://images.unsplash.com/photo-1482192596544-9eb780fc7f66?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=4d3b7a4a9f6a2b9a8c3f8d7c1b0a2b3f'
  },
  {
    id: 'closing',
    title: "Let's Make Memories!",
    text: ['No matter how the photos turn out — the best part is being together. Let’s laugh, explore, and fill Lenirra with Cholilah energy!', '“The smiles, the chaos, the love — let’s capture it all.”', 'See you at Lenirra!'],
    bg: 'https://images.unsplash.com/photo-1470770903676-69b98201ea1c?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=9f8f7f6e5d4c3b2a1f0e9d8c7b6a5f4d'
  }
];

export default function App() {
  return (
    <div className="font-poppins bg-cream text-gray-800">
      <Header sections={SECTIONS} />
      <main>
        {SECTIONS.map((sec, idx) => (
          <Section key={sec.id} sec={sec} idx={idx} />
        ))}
      </main>
      <Footer />
    </div>
  );
}

function Section({ sec, idx }) {
  return (
    <section
      id={sec.id}
      className="section-min relative bg-cover bg-center flex items-center justify-center"
      style={{
        backgroundImage: `url(${sec.bg})`
      }}
    >
      <div className="absolute inset-0 site-overlay"></div>

      <motion.div
        initial={{ opacity: 0, y: 30 }}
        whileInView={{ opacity: 1, y: 0 }}
        viewport={{ once: true }}
        transition={{ duration: 0.6, delay: idx * 0.05 }}
        className="relative z-10 max-w-4xl mx-6 md:mx-0 p-8 glass-card"
      >
        <div className="flex items-center gap-3 mb-3">
          <span className="sticker">{idx === 0 ? '🌞🌾⛰🏕📸' : '✨'}</span>
          <h2 className="text-xl md:text-2xl font-semibold">{sec.title}</h2>
        </div>

        {sec.subtitle && <p className="text-sm italic mb-4">{sec.subtitle}</p>}

        {sec.mini && <p className="text-lg font-handwritten mb-4">{sec.mini}</p>}

        {sec.text && typeof sec.text === 'string' && <p className="mb-4 whitespace-pre-line">{sec.text}</p>}

        {sec.rows && (
          <ul className="grid gap-2 mb-4 list-inside">
            {sec.rows.map((r, i) => (
              <li key={i} className="flex items-start gap-3">
                <Camera size={18} className="mt-1" /> <span>{r}</span>
              </li>
            ))}
          </ul>
        )}

        {sec.activities && (
          <ul className="grid grid-cols-2 md:grid-cols-3 gap-2 mb-4">
            {sec.activities.map((a, i) => (
              <li key={i} className="flex items-center gap-2 bg-white/90 rounded-md p-2 text-sm shadow-sm">
                <Sun size={18} /> {a}
              </li>
            ))}
          </ul>
        )}

        {sec.colors && (
          <div className="grid grid-cols-2 md:grid-cols-5 gap-3">
            {sec.colors.map((c) => (
              <div key={c.hex} className="color-chip" style={{ background: c.hex }}>
                <div className="text-xs font-semibold">{c.label}</div>
                <div className="text-[10px] mt-1">{c.hex}</div>
              </div>
            ))}
          </div>
        )}

        {sec.text && Array.isArray(sec.text) && (
          <ul className="mt-4 space-y-2">
            {sec.text.map((t, i) => (
              <li key={i} className="flex items-start gap-3">
                <span className="text-base">•</span>
                <span>{t}</span>
              </li>
            ))}
          </ul>
        )}

        {/* small divider */}
        <div className="section-divider" />
        {/* last small CTA or tip */}
        {sec.text && idx === 3 && <p className="text-sm italic">Bring hats, baskets, and a good mood ✨</p>}
        {
import React from 'react';

export default function Header({ sections }) {
  return (
    <header className="fixed top-4 left-1/2 transform -translate-x-1/2 z-40">
      <nav className="bg-white/90 backdrop-blur-md glass-card px-4 py-2 flex gap-3 items-center">
        <a href="#cover" className="font-semibold">Cholilah • Lenirra</a>
        <div className="hidden md:flex gap-2">
          {sections.slice(0, sections.length).map(s => (
            <a key={s.id} href={`#${s.id}`} className="text-sm px-2 py-1 rounded hover:underline">{s.title.split(':')[0]}</a>
          ))}
        </div>
      </nav>
    </header>
  );
}
import React from 'react';

export default function Footer() {
  return (
    <footer className="py-8 text-center text-sm text-gray-600">
      <div className="max-w-3xl mx-auto">Made with 💚 for Cholilah • Lenirra • 6–7 December 2025</div>
    </footer>
  );
}
