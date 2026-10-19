<script setup>
import { ref } from 'vue'

const profile = ref({
  name: 'ArtcDragon',
  handle: '@ArtcDragon',
  bio: 'Up and coming content creator and streamer These links are all my socials Xen Recruitment Challenge!!!!',
  avatar: 'https://unavatar.io/youtube/Artcdrgn',
})

const links = ref([
  {
    title: 'Twitch Channel',
    url: 'https://twitch.tv/artcdragon/home',
    badge: 'Live',
    accent: '#a855f7'
  },
  {
    title: 'YouTube',
    url: 'https://www.youtube.com/@Artcdrgn',
    accent: '#ef4444'
  },
  {
    title: 'Instagram',
    url: 'https://www.instagram.com/artcdrgn/',
    accent: '#ec4899'
  },
  {
    title: 'Discord Community (The Artc Palace)',
    url: 'https://discord.com/invite/sSW7C82aGv',
    accent: '#6366f1'
  },
  {
    title: 'TikTok',
    url: 'https://www.tiktok.com/@artcdragon',
    accent: '#06b6d4'
  }
])
</script>

<template>
  <div class="page-container">
    <!-- Glow Effects -->
    <div class="glow glow-top"></div>
    <div class="glow glow-bottom"></div>

    <main class="content-wrapper">
      <!-- Profile Header -->
      <header class="profile-header">
        <div class="avatar-ring">
          <img :src="profile.avatar" :alt="profile.name" class="avatar-img" />
        </div>
        <h1 class="profile-title">{{ profile.name }}</h1>
        <p class="profile-handle">{{ profile.handle }}</p>
        <p class="profile-bio">{{ profile.bio }}</p>
      </header>

      <!-- Links Stack -->
      <div class="links-stack">
        <a 
          v-for="(link, index) in links" 
          :key="index"
          :href="link.url"
          target="_blank"
          rel="noopener noreferrer"
          class="link-card"
          :style="{ '--hover-accent': link.accent }"
        >
          <span class="link-title">{{ link.title }}</span>
          <div class="link-meta">
            <span v-if="link.badge" class="badge">{{ link.badge }}</span>
            <svg class="external-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
            </svg>
          </div>
        </a>
      </div>
    </main>

    <!-- Footer Credit -->
    <footer class="footer">
      made by 
      <a href="https://lyrafoxwood.com" target="_blank" rel="noopener noreferrer" class="footer-link">
        lyrafoxwood
      </a> 
      with love ❤️
    </footer>
  </div>
</template>

<style scoped>
.page-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  padding: 2rem 1rem;
  position: relative;
  overflow: hidden;
}

/* Background Glows */
.glow {
  position: absolute;
  width: 350px;
  height: 350px;
  border-radius: 50%;
  filter: blur(100px);
  pointer-events: none;
  opacity: 0.15;
}

.glow-top {
  top: -100px;
  left: -100px;
  background: #a855f7;
}

.glow-bottom {
  bottom: -100px;
  right: -100px;
  background: #2dd4bf;
}

/* Content Container */
.content-wrapper {
  width: 100%;
  max-width: 420px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.75rem;
  z-index: 10;
  margin: auto 0;
}

/* Profile Styling */
.profile-header {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.avatar-ring {
  width: 112px;
  height: 112px;
  border-radius: 50%;
  padding: 3px;
  background: linear-gradient(135deg, #a855f7, #2dd4bf);
  margin-bottom: 1rem;
  box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5);
}

.avatar-img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}

.profile-title {
  font-size: 1.5rem;
  font-weight: 800;
  color: #ffffff;
  margin-bottom: 0.25rem;
}

.profile-handle {
  font-size: 0.875rem;
  font-weight: 600;
  color: #2dd4bf;
  margin-bottom: 0.5rem;
}

.profile-bio {
  font-size: 0.8125rem;
  color: #94a3b8;
  max-width: 280px;
  line-height: 1.4;
}

/* Links Stack */
.links-stack {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 0.875rem;
}

.link-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 1.25rem;
  border-radius: 12px;
  background: rgba(15, 23, 42, 0.75);
  border: 1px solid rgba(255, 255, 255, 0.08);
  color: #f8fafc;
  text-decoration: none;
  backdrop-filter: blur(12px);
  transition: all 0.25s ease;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
}

.link-card:hover {
  transform: translateY(-2px);
  border-color: var(--hover-accent);
  box-shadow: 0 8px 20px -4px rgba(0, 0, 0, 0.5);
}

.link-title {
  font-weight: 600;
  font-size: 0.95rem;
}

.link-meta {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.badge {
  font-size: 0.65rem;
  font-weight: 700;
  text-transform: uppercase;
  padding: 0.2rem 0.5rem;
  border-radius: 9999px;
  background: rgba(239, 68, 68, 0.2);
  color: #f87171;
  border: 1px solid rgba(239, 68, 68, 0.3);
}

.external-icon {
  width: 16px;
  height: 16px;
  color: #64748b;
  transition: color 0.2s ease;
}

.link-card:hover .external-icon {
  color: #f8fafc;
}

/* Footer */
.footer {
  text-align: center;
  font-size: 0.8125rem;
  color: #64748b;
  z-index: 10;
  padding-top: 1rem;
}

.footer-link {
  color: #2dd4bf;
  text-decoration: none;
  font-weight: 600;
  transition: color 0.2s ease;
}

.footer-link:hover {
  color: #5eead4;
  text-decoration: underline;
}
</style>