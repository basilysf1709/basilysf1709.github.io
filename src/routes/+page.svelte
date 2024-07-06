<script lang="ts">
  import { ArrowUpRight } from "lucide-svelte";

  import Seo from "$lib/components/Seo.svelte";

  const featuredProjects = [
    {
      name: "dockermake",
      href: "https://github.com/basilysf1709/dockermake",
      desc: "add a makefile for your docker",
    },
    {
      name: "design patterns",
      href: "https://github.com/basilysf1709/tcp-server-design-patterns",
      desc: "design patterns in low-level C++ networking"
    },
    {
      name: "teachify",
      href: "https://github.com/UsmanBasilAgency/teachify",
      desc: "Fully administered AI tool to help professors and students in their daily tasks",
      aside: "Backed by Prof. Judi McCuaig"
    },
    {
      name: "getquranverse",
      href: "https://github.com/basilysf1709/getquranverse",
      desc: "Quran Trivia with friends",
      aside: "2000 visitors"
    },
    {
      name: "rate-limiter",
      href: "https://github.com/basilysf1709/rate-limiting-as-a-service",
      desc: "Implementing rate limiting algorithms in go"
    },
  ];
</script>

<Seo
  title="Basil Yusuf"
  description="Software engineer, researcher, and reader. Making meaningful systems and interfaces for people."
/>

<p
  class="layout-md text-black text-xl leading-tight font-light mb-16"
  id="eric-is"
>
  <span class="g">is a</span> software engineer<span class="g">,</span><br />
  researcher<span class="g">, and</span><br />
  reader<span class="g">.</span>
</p>

<div class="layout-md text-lg space-y-14">
  <div class="space-y-5">
    <p>
      I am an Incoming Software Engineer at <a class="link" href="https://hubspot.com">HubSpot</a>, a
      leading CRM platform.
    </p>

    <p>
      I am deeply passionate about developing software that solves hard technical problems at scale.
    </p>

    <p>
      In this pursuit, I aspire to become a specialist with deep domain-specific knowledge in Platform, Infrastructure, and Distributed Systems. I aim to master the intricacies of designing and managing scalable, robust, and efficient systems that can support a wide range of applications. My goal is to contribute to the development of cutting-edge technologies that enhance user experiences and drive innovation in the field of software engineering.
    </p>
  </div>

  <div class="leading-snug space-y-4">
    <p class="pb-2">Notable projects:</p>

    {#each featuredProjects as project}
      <a class="project-pair" href={project.href}>
        <div class="text-black font-medium">
          {project.name}
          <ArrowUpRight size={18} class="inline text-neutral-400" />
        </div>
        <div>
          <p>{project.desc}</p>
          {#if project.aside}
            <aside>{project.aside}</aside>
          {/if}
        </div>
      </a>
    {/each}
  </div>

  <div class="space-y-5">
    <p>
      Previously, I worked at <a class="link" href="https://deloitte.com"
        >Deloitte</a
      >, <a class="link" href="https://www.amazon.ca/ftu/home">Amazon</a>,
      <a class="link" href="https://td.com">TD Bank</a>, and
      <a class="link" href="https://interac.ca">Interac</a>. I’ve also
      independently published things in the past, like an article on
      <a
        class="link"
        href="https://medium.com/@basilyusuf1709/docker-commands-are-long-and-boring-heres-a-better-approach-5b3e1bfef481"
        >docker</a
      >, and
      <a class="link" href="https://github.com/basilysf1709/tcp-server-design-patterns"
        >low-level networking</a
      >
      for research. Additionally, I have also won
      <a class="link" href="https://devpost.com/basilyusuf1709"
        >three hackathons</a
      >.
    </p>

    <p>
      I recently graduated from University of Guelph, where I was a
      <a class="link" href="https://medium.com/@basilyusuf1709/skill-based-matchmaking-architecture-sbmm-open-source-0f1184b8ceb2"
        >Research Associate</a
      > on Open Source Skill-based Matchmaking Architecture (SBMM) and a <a class="link" href="https://www.uoguelph.ca/registrar/calendars/undergraduate/2019-2020/courses/cis2430.shtml"
      >Teaching Assistant</a> for Object-oriented Programming (CIS*2430).
    </p>

    <p>Other interests: russian philosophy, islamic theology, geopolitics, history.</p>
  </div>
</div>

<style lang="postcss">
  .g {
    @apply text-neutral-400;
  }

  em {
    @apply font-serif text-[110%] leading-[100%];
  }

  .project-pair {
    @apply grid sm:grid-cols-[1fr,2fr] gap-y-1 -mx-3 px-3 py-2 hover:bg-neutral-100 transition-colors;
  }

  aside {
    @apply mt-0.5 text-base text-neutral-500;
  }

  /* Correction for vertical navigation links on mobile. */
  @media (max-width: 420px) {
    #eric-is {
      @apply -mt-10;
    }
  }
</style>
