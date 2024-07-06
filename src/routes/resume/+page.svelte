<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import Workplace from "./Workplace.svelte";
</script>

<Seo
  title="Basil Yusuf – Resume"
  description="Software engineer, researcher, and designer. Making meaningful systems and interfaces for people."
/>

<section class="layout-md py-6">
  <h2 class="heading2">Education</h2>

  <div class="mb-4">
    <div class="flex justify-between items-end">
      <h3 class="text-black text-lg">University of Guelph</h3>
      <div class="text-neutral-500 mb-0.5">Sep 2020 – Apr 2024</div>
    </div>
    <p class="byline">Bachelor of Computing, Computer Science and Economics</p>
  </div>
</section>

<section class="layout-md py-6">
  <h2 class="heading2">Work Experience</h2>

  <Workplace
    title="Backend & Infrastructure Engineer (Contract)"
    company="Deloitte"
    url="https://www2.deloitte.com/us/en/pages/risk/solutions/cyber-incident-response-services.html"
    dates="Sep 2023 – Jul 2024"
    location="Toronto, Ontario"
  >
    <li>Transitioned from manual deployments to Continuous Deployment (CD) by building a Deployment Pipeline that tests and deploys directly to AWS infrastructure, reducing deployment time from 20 minutes to less than 5 minutes.</li>
    <li>Built a Python-based AWS Lambda Scheduler to run daily jobs that fetch new cybersecurity incidents, enhancing the timeliness and effectiveness of our incident response and monitoring systems.</li>
    <li>Implemented an Application Load Balancer in AWS for efficient traffic distribution across multiple Fargate instances, reducing downtime from 15 minutes to 0 seconds for each deployment.</li>
    <li>Developed and configured Docker containers for React.js, MongoDB, Express/GraphQL, and Nginx, successfully deploying them on AWS ECS - Fargate, within a secure VPC environment, ensuring robust security measures.</li>
    <li>Implemented AWS Secrets Manager Password Rotation for DocumentDB cluster security in TypeScript, regularly updating access credentials for enhanced database security and compliance.</li>
  </Workplace>

  <Workplace
    title="Software Engineer Intern"
    company="Amazon"
    url="https://www.amazon.com/ftu/home"
    dates="May 2023 – Aug 2023"
    location="Toronto, Ontario"
  >
    <li>Engineered a web app for Amazon Kids+ to fetch subscription offers from different regions, attach metadata to offers, and update customer eligibility for offers, reducing processing time from 3-5 minutes to less than 5 seconds.</li>
    <li>Lowered subscription service downtime from 5 minutes to ∼0.1 seconds by automating AWS Systems Manager configuration (AWS AppConfig) deployments for customer eligibility using Java and AWS CDK.</li>
    <li>Developed and deployed Virtual Private Cloud (VPC) and AWS Lambda infrastructure using AWS CDK (TypeScript), ensuring secure connections by adding IAM roles for enhanced deployment and connectivity.</li>
  </Workplace>

  <Workplace
    title="Software Engineer Intern"
    company="TD Bank"
    url="https://www.td.com/us/en/personal-banking"
    dates="Jan 2023 – Apr 2023"
    location="Toronto, Ontario"
  >
    <li>Migrated 9 SOAP API endpoints to 3 REST API endpoints in Java and Spring Boot using OpenAPI specifications that scale to over a million customers, resulting in reduction of production downtime from 5 minutes to less than 1 second.</li>
    <li>Devised a robust XML parser using Python that seamlessly converted 9 endpoints from XML to JSON, boosting data accessibility for other engineers on the team by 75% and significantly reducing parsing time by 90%.</li>
  </Workplace>

  <Workplace
    title="Software Engineer Intern (Platform and Cloud Architecture)"
    company="Interac"
    url="https://www.interac.ca/en/consumers/products/interac-e-transfer/"
    dates="Sep 2022 – Dec 2022"
    location="Toronto, Ontario"
  >
    <li>Developed authentication infrastructure of Interac e-Transfers in Canada using Azure Key Vault, Azure Stack Hub, and Azure Identity Management of a system that drives 371.4 million highly secure transactions every day.</li>
    <li>Initiated and coordinated building of Interac’s Digital Platform architecture and infrastructure, used by Canadians 660,000 times daily, through Jira assignments and documenting Proof-of-Concepts for other Architects.</li>
  </Workplace>
</section>

<section class="layout-md py-6">
  <h2 class="heading2">University Experience</h2>

  <Workplace
    title="Undergraduate Researcher (C++)"
    company="University of Guelph"
    url="https://www.uoguelph.ca"
    dates="Jan 2024 – Apr 2024"
    location="Guelph, Ontario"
  >
    <li>Developed a modular TCP server in C++ using advanced OOP design patterns such as Singleton, Builder, and Decorator, which streamlined the integration of security/logging features, significantly boosting system adaptability.</li>
    <li>Optimized a C++ TCP server by implementing a robust observer-subject framework, which enhanced real-time event logging and observer management, thereby handling multiple client connections simultaneously.</li>
  </Workplace>

  <Workplace
    title="Research Associate (System Design)"
    company="University of Guelph"
    url="https://www.uoguelph.ca"
    dates="Jan 2023 – Apr 2023"
    location="Guelph, Ontario"
  >
    <li>Developed architecture design for a sophisticated game matchmaking server, which integrated microservices and RabbitMQ to drive substantial scalability and streamline communication between players and servers.</li>
    <li>Executed the seamless integration of MongoDB as a cornerstone for secure player data storage, ensuring uninterrupted game progress preservation and streamlined query operations for enhanced system responsiveness.</li>
  </Workplace>

  <Workplace
    title="Teaching Assistant (OOP)"
    company="University of Guelph"
    url="https://www.uoguelph.ca"
    dates="Jan 2023 – Apr 2023"
    location="Guelph, Ontario"
  >
    <li>Led 75+ one-on-one tutoring sessions to solidify students' concepts on Object-Oriented Programming and JUnit Testing.</li>
    <li>Conducted 85+ interviews to assess students' grasp of course content, along with grading of tests and assignments.</li>
  </Workplace>
</section>

<style lang="postcss">
  b {
    @apply font-medium;
  }

  ul {
    @apply list-disc pl-7 marker:text-neutral-400;
  }

  .byline {
    @apply font-serif italic;
  }
</style>
