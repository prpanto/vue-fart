<template>
  <div class="max-w-2xl mx-auto">
    <div class="mt-10 flex flex-wrap justify-center gap-4">
      <div
        v-for="(fart, index) in farts"
        :key="index"
        class="px-4 py-2 flex flex-col justify-center items-center space-x-4 rounded-md shadow-md bg-white"
        @click="playSound(`./assets/farts/${fart.file}`)"
      >
        <SpeakerWaveIcon class="w-10 h-10" />
        {{ fart.name }}
      </div>
    </div>
  </div>
</template>

<script setup>
import { SpeakerWaveIcon } from '@heroicons/vue/24/outline'

const farts = [
  { name: 'Toot', file: 'fart1.wav' },
  { name: 'Jack the Ripper', file: 'fart2.wav' },
  { name: 'Snap Crackle Plop', mp3: 'fart3.mp3', file: 'fart3.wav' },
  { name: 'Squit', file: 'fart4.wav' },
  { name: 'Squat', file: 'fart5.wav' },
  { name: 'Raspberry', file: 'fart6.wav' },
  { name: 'Tuppence', file: 'fart7.wav' },
  { name: 'Lift Off', file: 'fart8.wav' },
  { name: 'Trouser Trumpet', file: 'fart9.wav' },
  { name: 'The Fizzler', file: 'fart10.wav' },
  { name: 'Windy Valley', file: 'fart11.wav' },
  { name: 'Eine Kleine Fartmusik', file: 'fart12.wav' },
  { name: 'Fartception ', file: 'fart13.wav' },
  { name: 'Point', file: 'fart14.wav' },
]

function playSound(file) {
  const audio = new Audio(file)
  audio.play()
}
</script>