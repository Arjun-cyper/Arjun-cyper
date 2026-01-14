<script setup>
import { Github, Mail, ExternalLink, Code2, Terminal } from 'lucide-react';

const accounts = [
  {
    title: "ArjunLevi",
    role: "Primary Developer",
    email: "66naga18@gmail.com",
    color: "from-blue-600 to-cyan-500",
    description: "Main workspace for core development and long-term project stability."
  },
  {
    title: "Arjun-cyper",
    role: "Security & Research",
    email: "18naga66@gmail.com",
    color: "from-purple-600 to-pink-500",
    description: "Experimental repository for cyber research, automation, and Frame development."
  }
];
</script>

<template>
  <div class="min-h-screen bg-slate-900 text-slate-100 p-8">
    <header class="max-w-6xl mx-auto mb-12 flex justify-between items-center">
      <div>
        <h1 class="text-4xl font-bold bg-gradient-to-r from-white to-slate-400 bg-clip-text text-transparent">
          Vue Developer Console
        </h1>
        <p class="text-slate-400 flex items-center gap-2 mt-2">
          <Terminal :size="16" /> Active Identity: Arjun
        </p>
      </div>
    </header>

    <main class="max-w-6xl mx-auto grid md:grid-cols-2 gap-8">
      <div v-for="acc in accounts" :key="acc.title" 
           class="bg-slate-800/50 border border-slate-700 rounded-2xl p-6 hover:border-slate-500 transition-all group">
        <div :class="`w-12 h-12 rounded-lg bg-gradient-to-br ${acc.color} mb-6 flex items-center justify-center`">
          <Github class="text-white" />
        </div>
        
        <h2 class="text-2xl font-bold mb-1">{{ acc.title }}</h2>
        <p class="text-cyan-400 text-sm font-mono mb-4">{{ acc.role }}</p>
        <p class="text-slate-400 mb-6 leading-relaxed">{{ acc.description }}</p>

        <div class="space-y-3 border-t border-slate-700 pt-6">
          <div class="flex items-center gap-3 text-slate-300">
            <Mail :size="18" class="text-slate-500" />
            <span>{{ acc.email }}</span>
          </div>
          <div class="flex items-center gap-3 text-slate-300">
            <ExternalLink :size="18" class="text-slate-500" />
            <span>github.com/{{ acc.title }}</span>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>