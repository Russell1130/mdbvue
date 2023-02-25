
<template>
  <div>
  <Disclosure as="nav" class="bg-white-800" v-slot="{ open }">
    <div class="mx-auto max-w-7xl px-2 sm:px-6">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <DisclosureButton class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-100 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white">
            <span class="sr-only">Open main menu</span>
            <Bars3Icon v-if="!open" class="block h-6 w-6" aria-hidden="true" />
            <XMarkIcon v-else class="block h-6 w-6" aria-hidden="true" />
          </DisclosureButton>
        </div>
        <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex flex-shrink-0 items-center">
            <img class="block h-8 w-auto lg:block" src="logo.png" alt="Your Company" />
          </div>
        </div>
        <div class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0 sm:block font-black hidden">
          <a v-for="item in navigation" :key="item.name" :href="item.href" :class="[item.current ? 'bg-gray-900 text-white' : 'text-black-300 hover:bg-gray-100 hover:text-black', 'px-3 py-2 rounded-md text-sm font-medium']" :aria-current="item.current ? 'page' : undefined">{{ item.name }}</a>
        </div>
      </div>
    </div>

    <DisclosurePanel class="sm:hidden">
      <div class="space-y-1 px-2 pt-2 pb-3">
        <DisclosureButton v-for="item in navigation" :key="item.name" as="a" :href="item.href" :class="[item.current ? 'bg-gray-900 text-black' : 'text-black-900 hover:bg-gray-100 hover:text-black', 'block px-3 py-2 rounded-md text-base font-medium']" :aria-current="item.current ? 'page' : undefined">{{ item.name }}</DisclosureButton>
      </div>
    </DisclosurePanel>
  </Disclosure>
  <div class="flex flex-col bg-gray-200 rounded-3 mx-2 md:flex-row md:mx-9 md:px-20">
      <div class="w-3/4 self-center pt-16 pb-8">
        <img src="human.png" class="py-5"/>
        <button class="bg-white rounded-md p-2">Learn More</button>
      </div>
      <div class="w-2/4 self-center">
        <img src="right.png"/>
      </div>
    </div>
    <div class="flex flex-col pr-20 md:flex-row md:px-20">
      <div class="w-full self-center pt-16 md:w-2/4">
        <img src="hmt.png" class="py-5"/>
      </div>
      <div class="w-full self-center text-3xl pl-10 text-purple-800 md:w-2/5">
        <nobr class=" text-purple-600">HMT</nobr> funds the processing of digitized work, and rewards workers for their contributions.
      </div>
    </div>
    <div class="bg-violet-50 w-full flex flex-col">
      <div class="w-2/3 self-center">
        <div class="text-purple-800 text-4xl pt-5 pl-5">Token Details</div>
        <img src="token.png" />
        <img src="tokentype.png" class="pl-5"/>
        <img src="smart.png" class="pl-7 pb-10"/>
        <img src="exchanges.png" class="pl-7"/>
      </div>
    </div>
    <div class="flex flex-col bg-violet-50 rounded-3xl px-20 m-20">
      <div class="self-center p-10 text-purple-800 text-4xl">HUMAN in the media</div>
      <div class="self-center">
        <img src="bitcoin.png"/>
      </div>
    </div>
    <div class="flex flex-col">
      <div class="flex flex-col self-center w-full p-10">
        <div class="text-purple-800 text-4xl">Token Allocation</div>
        <Doughnut class="w-1/2 self-center" />
      </div>
    </div>
    <div class="flex flex-col">
      <div class="flex flex-col self-center w-full p-10">
        <div class="text-purple-800 text-4xl">Supply Over Time</div>
        <Linechart class="w-2/3 self-center" />
      </div>
    </div>
    <div class="flex flex-col bg-violet-50 rounded-3xl m-20 pb-12">
      <div class="self-center p-10 text-purple-800 text-4xl " >How do i get HMT?</div>
      <div class="self-center flex flex-col md:flex-row ">
        <img src="complete.png" class=" bg-white w-full md:w-1/6 m-auto"/>
        <img src="grants.png" class=" bg-white w-full md:w-1/6 m-auto"/>
        <img src="ambassador.png" class=" bg-white w-full md:w-1/6 m-auto"/>
        <img src="refer.png" class=" bg-white w-full md:w-1/6 m-auto"/>
        <img src="validator.png" class=" bg-white w-full md:w-1/6 m-auto"/>
      </div>
    </div>
    <br/>
    <div class="flex flex-col bg-violet-50 rounded-3xl m-20 pb-6">
      <div class="self-center p-10 text-purple-800 text-4xl">Utility of the HUMAN Token</div>
      <div class="self-center flex flex-col md:flex-row">
        <img src="job.png" class="md:w-1/3 w-full"/>
        <img src="worker.png" class="md:w-1/3 w-full"/>
        <img src="validators.png" class="md:w-1/3 w-full"/>
      </div>
    </div>
    <div class="flex flex-col">
      <div class="self-center text-purple-800 text-4xl">Disclaimer</div>
      <div class="self-center px-5 text-purple-800 text-base">The HUMAN Protocol Foundation makes no representation, warranty, or undertaking, express or implied, as to the accuracy, reliability, completeness, or reasonableness of the Information. Any assumptions, opinions, and estimates expressed in the information on this page constitutes the HUMAN Protocol Foundation’s judgment as of 18/11/21 and are subject to change without notice. The HUMAN Protocol Foundation does not accept any liability for any direct, consequential or other loss arising from reliance on the contents of the information in this graphic.</div>
    </div>
    <div class="flex flex-col pt-12">
      <div class="flex self-center w-4/5">
        <div class="w-5/6 text-purple-800 font-bold text-2xl">Recent Entries</div>
        <button class="border-purple-800 border-2 p-2 rounded-lg w-1/6 mr-0">Go to blog</button>
      </div>
    </div>
    <div class="flex flex-col w-full pb-16">
      <div class="w-1/2 self-center">
        <img src="recent.png"/>
        <div class="flex flex-row pt-4">
          <div class="text-purple-800 text-base self-center pr-10">Mar 31 2022</div>
          <button class="border-purple-800 border-2 p-2 rounded-lg mr-0">Guest post</button>
        </div>
        <div class="text-purple-800 text-xl self-center font-bold">Interview with Andreas Schemm, Head of Ecosystem Development & Operations at HUMAN Protocol</div>
      </div>
    </div>

    <!-- Section: Social media -->
    <div class="flex flex-col">
      <div class="flex flex-col w-full md:flex-row self-center md:w-11/12">
        <div class="flex flex-col md:w-6/12">
          <div class="w-5/6 text-purple-800 font-bold text-2xl pb-2">Get HUMAN news and updates</div>
          <div class="w-full">
            <input type="text" class="border-purple-800 border-2 rounded-md w-4/6 p-1" />
            <button class="bg-purple-800 border-2 rounded-md p-2 px-4 text-white">Subscribe</button>
          </div>
          <div class="text-purple-800">By subscribing you agree to our Privacy Policy</div>
        </div>
        <div class="w-3/12"></div>
        <div class="md:w-5/12 self-center">
          <i class="fas fa-dove text-purple-800 m-3 fa-2x"></i>
          <i class="fab fa-twitter text-purple-800 m-3 fa-2x"></i>
          <i class="fab fa-github-square text-purple-800 m-3 fa-2x"></i>
          <i class="fab fa-linkedin-in text-purple-800 m-3 fa-2x"></i>
          <i class="fab fa-youtube text-purple-800 m-3 fa-2x"></i>
        </div>
      </div>
    </div>
    <!-- Section: Social media -->
    <!-- Section: Links  -->
    <div class="flex flex-col md:flex-row">
      <div class="md:w-1/6 pb-5">
        <h6 class="text-uppercase fw-bold mb-4">Products</h6>
        <div class="text-reset">HUMAN App</div>
        <div class="text-reset">Proof of HUMANity</div>
        <div class="text-reset">IMOO</div>
      </div>
      <div class="md:w-1/6 pb-5">
        <h6 class="text-uppercase fw-bold mb-4">Discover</h6>
        <div class="text-reset">Token</div>
        <div class="text-reset">Routing Layer</div>
        <div class="text-reset">Team</div>
        <div class="text-reset">Careers</div>
      </div>
      <div class="md:w-1/6 pb-5">
        <h6 class="text-uppercase fw-bold mb-4">Build</h6>
        <div class="text-reset">Developers</div>
        <div class="text-reset">Technology</div>
        <div class="text-reset">DevBounty Program</div>
        <div class="text-reset">BugBounty Program</div>
        <div class="text-reset">Github</div>
        <div class="text-reset">Grants Program</div>
      </div>
      <div class="md:w-1/6 pb-5">
        <h6 class="text-uppercase fw-bold mb-4">Community</h6>
        <div class="text-reset">Grants Program</div>
        <div class="text-reset">Elite Ops Program</div>
        <div class="text-reset">Events</div>
      </div>
      <div class="md:w-1/6 pb-5">
        <h6 class="text-uppercase fw-bold mb-4">Resources</h6>
        <div class="text-reset">Documents Hub</div>
        <div class="text-reset">Litepaper</div>
        <div class="text-reset">Technical Whitepaper</div>
        <div class="text-reset">AI Whitepaper</div>
        <div class="text-reset">System Status</div>
        <div class="text-reset">In The News</div>
        <div class="text-reset">One Pagers Archive</div>
        <div class="text-reset">Brand Assets</div>
      </div>
      <div class="md:w-1/6 pb-5">
        <h6 class="text-uppercase fw-bold mb-4">Impact Projects</h6>
        <div class="text-reset">Blog</div>
        <div class="text-reset">Explorer</div>
        <div class="text-reset">Mixin</div>
        <div class="text-reset">Careers</div>
      </div>
    </div>
    <!-- Section: Links  -->
    <!-- Copyright -->
    <div class="text-center p-4" style="background-color: rgba(0, 0, 0, 0.05)">
      © 2021 Copyright:
      <a class="text-reset fw-bold" href="https://mdbootstrap.com/">MDBootstrap.com</a>
    </div>
  </div>
  
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel, Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
import { Bars3Icon, BellIcon, XMarkIcon } from '@heroicons/vue/24/outline'
import Doughnut from './Doughnut.vue';
import Linechart from './Linechart.vue'

const navigation = [
  { name: 'Products', href: '#', current: false },
  { name: 'Code', href: '#', current: false },
  { name: 'Ecosystem', href: '#', current: false },
  { name: 'Team', href: '#', current: false },
  { name: 'Resources', href: '#', current: false },
  { name: 'Join', href: '#', current: false },
]

</script>

<style scoped>
.read-the-docs {
  color: #050505;
}
</style>
