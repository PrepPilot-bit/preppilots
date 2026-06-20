import React from "react";
import { motion } from "framer-motion";
import {
  ArrowRight,
  CheckCircle2,
  Compass,
  Clock3,
  Flame,
  LineChart,
  Sparkles,
  Target,
  Zap,
} from "lucide-react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const features = [
  {
    icon: Target,
    title: "Exam Countdown",
    description:
      "Track your exam date, remaining days, and daily targets in one focused dashboard.",
  },
  {
    icon: Clock3,
    title: "Smart Study Planner",
    description:
      "Break your syllabus into subjects, chapters, and revision milestones automatically.",
  },
  {
    icon: LineChart,
    title: "Progress Analytics",
    description:
      "See study hours, streaks, completion rate, and weak areas with visual insights.",
  },
  {
    icon: Flame,
    title: "Streak Motivation",
    description:
      "Stay consistent with streaks, badges, and small wins that keep momentum alive.",
  },
  {
    icon: Sparkles,
    title: "AI Readiness Score",
    description:
      "Estimate how prepared you are and know exactly what to focus on next.",
  },
  {
    icon: Zap,
    title: "Fast, Simple, Mobile-First",
    description:
      "Built to work smoothly on phone and laptop with a distraction-free interface.",
  },
];

const steps = [
  {
    title: "Add your exam",
    text: "Choose CA Foundation or another competitive exam and set the date.",
  },
  {
    title: "Plan your syllabus",
    text: "List subjects, chapters, and revision dates in a few clicks.",
  },
  {
    title: "Track daily progress",
    text: "Log study sessions and watch your readiness improve over time.",
  },
];

export default function PrepPilotLandingPage() {
  return (
    <div className="min-h-screen bg-slate-950 text-white">
      <div className="absolute inset-0 -z-10 overflow-hidden">
        <div className="absolute left-1/2 top-[-10rem] h-[28rem] w-[28rem] -translate-x-1/2 rounded-full bg-sky-500/20 blur-3xl" />
        <div className="absolute right-[-8rem] top-[18rem] h-[22rem] w-[22rem] rounded-full bg-amber-400/10 blur-3xl" />
      </div>

      <header className="mx-auto flex max-w-7xl items-center justify-between px-6 py-6 lg:px-8">
        <div className="flex items-center gap-3">
          <div className="flex h-11 w-11 items-center justify-center rounded-2xl bg-white/10 ring-1 ring-white/15 backdrop-blur">
            <Compass className="h-6 w-6 text-sky-300" />
          </div>
          <div>
            <p className="text-lg font-semibold tracking-tight">PrepPilot</p>
            <p className="text-xs text-white/60">Navigate your success</p>
          </div>
        </div>

        <Button className="rounded-full bg-white px-5 py-2 text-slate-950 hover:bg-slate-200">
          Join the waitlist
        </Button>
      </header>

      <main className="mx-auto max-w-7xl px-6 pb-20 lg:px-8">
        <section className="grid items-center gap-14 py-12 lg:grid-cols-2 lg:py-20">
          <motion.div
            initial={{ opacity: 0, y: 24 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6 }}
            className="max-w-xl"
          >
            <div className="mb-5 inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-4 py-2 text-sm text-white/80 backdrop-blur">
              <Sparkles className="h-4 w-4 text-amber-300" />
              Built for serious students who want structure
            </div>
            <h1 className="text-4xl font-bold tracking-tight text-white sm:text-5xl lg:text-6xl">
              Study smarter for every exam with one focused dashboard.
            </h1>
            <p className="mt-6 text-lg leading-8 text-white/70">
              PrepPilot helps students track exam dates, plan chapters, monitor study hours,
              and stay on course with a simple readiness score that shows real progress.
            </p>

            <div className="mt-8 flex flex-col gap-3 sm:flex-row">
              <Button className="rounded-full bg-sky-400 px-6 py-6 text-base font-semibold text-slate-950 hover:bg-sky-300">
                Start free <ArrowRight className="ml-2 h-4 w-4" />
              </Button>
              <Button
                variant="outline"
                className="rounded-full border-white/15 bg-white/5 px-6 py-6 text-base font-semibold text-white hover:bg-white/10"
              >
                See how it works
              </Button>
            </div>

            <div className="mt-8 flex flex-wrap gap-4 text-sm text-white/65">
              <span className="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-3 py-2">
                <CheckCircle2 className="h-4 w-4 text-emerald-400" />
                Mobile-first
              </span>
              <span className="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-3 py-2">
                <CheckCircle2 className="h-4 w-4 text-emerald-400" />
                Freemium ready
              </span>
              <span className="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-3 py-2">
                <CheckCircle2 className="h-4 w-4 text-emerald-400" />
                AI-powered planning
              </span>
            </div>
          </motion.div>

          <motion.div
            initial={{ opacity: 0, y: 24 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.75, delay: 0.08 }}
            className="relative"
          >
            <div className="absolute inset-0 rounded-[2rem] bg-gradient-to-br from-sky-500/20 via-transparent to-amber-400/10 blur-2xl" />
            <Card className="relative overflow-hidden rounded-[2rem] border-white/10 bg-white/8 shadow-2xl backdrop-blur-xl">
              <CardContent className="p-6 sm:p-8">
                <div className="flex items-center justify-between">
                  <div>
                    <p className="text-sm text-white/60">Your dashboard</p>
                    <h2 className="mt-1 text-2xl font-semibold">CA Foundation Readiness</h2>
                  </div>
                  <div className="rounded-full bg-emerald-400/15 px-3 py-1 text-sm text-emerald-300 ring-1 ring-emerald-400/20">
                    68% ready
                  </div>
                </div>

                <div className="mt-6 grid gap-4 sm:grid-cols-2">
                  <StatBox label="Days left" value="124" sub="until exam" />
                  <StatBox label="Study streak" value="18" sub="days straight" />
                  <StatBox label="Today" value="5.5h" sub="planned target" />
                  <StatBox label="Completed" value="41%" sub="syllabus done" />
                </div>

                <div className="mt-6 rounded-3xl border border-white/10 bg-slate-900/70 p-5">
                  <div className="flex items-center gap-2 text-sm text-white/70">
                    <Compass className="h-4 w-4 text-sky-300" />
                    Next best action
                  </div>
                  <p className="mt-3 text-lg font-medium">
                    Revise Business Economics and finish 2 remaining chapters today.
                  </p>
                  <div className="mt-4 h-2 w-full rounded-full bg-white/10">
                    <div className="h-2 w-[72%] rounded-full bg-gradient-to-r from-sky-400 to-amber-300" />
                  </div>
                </div>
              </CardContent>
            </Card>
          </motion.div>
        </section>

        <section className="py-6 lg:py-12">
          <div className="max-w-2xl">
            <p className="text-sm font-semibold uppercase tracking-[0.2em] text-sky-300">
              Features
            </p>
            <h2 className="mt-3 text-3xl font-bold tracking-tight sm:text-4xl">
              Everything needed to stay on track.
            </h2>
            <p className="mt-4 text-white/70">
              PrepPilot keeps the experience minimal while still giving students the structure,
              tracking, and accountability they need to finish strong.
            </p>
          </div>

          <div className="mt-10 grid gap-5 md:grid-cols-2 xl:grid-cols-3">
            {features.map((feature) => {
              const Icon = feature.icon;
              return (
                <Card
                  key={feature.title}
                  className="rounded-[1.75rem] border-white/10 bg-white/5 backdrop-blur"
                >
                  <CardContent className="p-6">
                    <div className="flex h-12 w-12 items-center justify-center rounded-2xl bg-sky-400/15 ring-1 ring-sky-300/20">
                      <Icon className="h-6 w-6 text-sky-300" />
                    </div>
                    <h3 className="mt-5 text-xl font-semibold">{feature.title}</h3>
                    <p className="mt-3 leading-7 text-white/70">{feature.description}</p>
                  </CardContent>
                </Card>
              );
            })}
          </div>
        </section>

        <section className="grid gap-6 py-12 lg:grid-cols-[1.1fr_0.9fr] lg:items-start">
          <Card className="rounded-[2rem] border-white/10 bg-white/5 backdrop-blur">
            <CardContent className="p-7 sm:p-8">
              <p className="text-sm font-semibold uppercase tracking-[0.2em] text-amber-300">
                How it works
              </p>
              <h2 className="mt-3 text-3xl font-bold tracking-tight">A simple flow that students actually use.</h2>
              <div className="mt-8 space-y-5">
                {steps.map((step, index) => (
                  <div key={step.title} className="flex gap-4 rounded-2xl border border-white/10 bg-slate-950/40 p-4">
                    <div className="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-white/10 font-semibold text-white">
                      {index + 1}
                    </div>
                    <div>
                      <h3 className="font-semibold">{step.title}</h3>
                      <p className="mt-1 text-white/70">{step.text}</p>
                    </div>
                  </div>
                ))}
              </div>
            </CardContent>
          </Card>

          <Card className="rounded-[2rem] border-white/10 bg-gradient-to-br from-sky-400/10 to-amber-300/10 backdrop-blur">
            <CardContent className="p-7 sm:p-8">
              <p className="text-sm font-semibold uppercase tracking-[0.2em] text-sky-300">
                Launch plan
              </p>
              <h2 className="mt-3 text-3xl font-bold tracking-tight">Built for a quick MVP and future growth.</h2>
              <ul className="mt-6 space-y-4 text-white/75">
                <li className="flex gap-3"><CheckCircle2 className="mt-1 h-5 w-5 text-emerald-400" />Start with countdown, planner, and streaks.</li>
                <li className="flex gap-3"><CheckCircle2 className="mt-1 h-5 w-5 text-emerald-400" />Add AI readiness scoring as the premium hook.</li>
                <li className="flex gap-3"><CheckCircle2 className="mt-1 h-5 w-5 text-emerald-400" />Grow from CA Foundation to more exams later.</li>
              </ul>
              <div className="mt-8 rounded-3xl border border-white/10 bg-slate-950/50 p-5">
                <p className="text-sm text-white/60">Suggested pricing</p>
                <div className="mt-2 flex items-end gap-2">
                  <span className="text-4xl font-bold">₹49</span>
                  <span className="pb-1 text-white/60">/month premium</span>
                </div>
              </div>
            </CardContent>
          </Card>
        </section>

        <section className="py-10">
          <div className="rounded-[2rem] border border-white/10 bg-white/5 px-6 py-10 text-center backdrop-blur sm:px-10">
            <p className="text-sm font-semibold uppercase tracking-[0.2em] text-sky-300">
              Ready to launch
            </p>
            <h2 className="mt-3 text-3xl font-bold tracking-tight sm:text-4xl">
              A serious brand for serious exam prep.
            </h2>
            <p className="mx-auto mt-4 max-w-2xl text-white/70">
              PrepPilot is positioned as a clean, modern productivity platform for students who want
              clarity, consistency, and confidence.
            </p>
            <div className="mt-7 flex flex-col justify-center gap-3 sm:flex-row">
              <Button className="rounded-full bg-sky-400 px-6 py-6 text-base font-semibold text-slate-950 hover:bg-sky-300">
                Launch website <ArrowRight className="ml-2 h-4 w-4" />
              </Button>
              <Button
                variant="outline"
                className="rounded-full border-white/15 bg-white/5 px-6 py-6 text-base font-semibold text-white hover:bg-white/10"
              >
                Customize branding
              </Button>
            </div>
          </div>
        </section>
      </main>
    </div>
  );
}

function StatBox({ label, value, sub }: { label: string; value: string; sub: string }) {
  return (
    <div className="rounded-3xl border border-white/10 bg-slate-950/50 p-5">
      <p className="text-sm text-white/60">{label}</p>
      <p className="mt-2 text-3xl font-bold">{value}</p>
      <p className="mt-1 text-sm text-white/50">{sub}</p>
    </div>
  );
}
