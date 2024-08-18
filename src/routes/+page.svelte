<script lang="ts">
  import { ArrowUpRight } from "lucide-svelte";

  import Seo from "$lib/components/Seo.svelte";

  const featuredProjects = [
    {
      name: "distributed systems",
      href: "https://github.com/basilysf1709/distributed-systems",
      desc: "comprehensive guide and algorithms on distributed systems implemented in zig",
    },
    {
      name: "chsim",
      href: "https://github.com/basilysf1709/chsim",
      desc: "consistent hashing ring simulation in zig",
    },
    {
      name: "lsm trees",
      href: "https://github.com/basilysf1709/btree-lsm-benchmark",
      desc: "ground up implementation of lsm trees in c++",
    },
    {
      name: "dockermake",
      href: "https://github.com/basilysf1709/dockermake",
      desc: "add a makefile for your docker",
      aside: "made this project after a reddit post got 100k views :)",
    },
    {
      name: "dynamodb",
      href: "https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf",
      desc: "deep dive into the architecture of Amazon's DynamoDB",
    },
    {
      name: "kubernetes",
      href: "https://medium.com/@basilyusuf1709/kubernetes-a-basic-overview-ad83bd92b727",
      desc: "completed a beginner course on kubernetes",
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
    <!-- <p>
      I am an Incoming Software Engineer at <a class="link" href="https://hubspot.com">HubSpot</a>, a
      leading CRM platform.
    </p> -->

    <p>
      I am deeply passionate about distributed systems, infrastructure and container orchestration.
    </p>
    <p>
      What truly amazes me is how things break in often unpredictable ways as systems scale. It's like watching a high-stakes game of Jenga played out in code and infrastructure. Each optimization, each new layer of complexity, adds both power and fragility. I'm obsessed with finding that sweet spot where performance, reliability, and maintainability converge, always pushing the envelope of what's possible in large-scale distributed computing. If you share the same level of passion as me, feel free to reach out to me on <a
        class="link"
        href="https://x.com/basilyusuf1709"
        >X</a
      >.
    </p>
  </div>

  <div class="leading-snug space-y-4">
    <p class="pb-2">What I have built and learned so far in 2024:</p>

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
    <p>Template by <a class="link" href="https://www.ekzhang.com/"
      >Eric Zhang</a
    ></p>
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
