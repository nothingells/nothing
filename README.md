import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function Home() {
  return (
    <main className="min-h-screen bg-[#0A0F2C] text-white px-4 py-10">
      <section className="text-center space-y-4">
        <h1 className="text-5xl font-bold text-yellow-400">nothing</h1>
        <p className="text-lg max-w-xl mx-auto text-gray-300">
          A Solana-based project focused on minimalism, transparency, and real innovation.
        </p>
        <div className="space-x-4">
          <a href="/whitepaper.pdf" target="_blank">
            <Button className="bg-yellow-500 text-black hover:bg-yellow-400">Read Whitepaper</Button>
          </a>
          <a href="https://discord.gg/your-invite" target="_blank">
            <Button variant="outline">Join Discord</Button>
          </a>
        </div>
      </section>

      <section className="mt-20 max-w-4xl mx-auto">
        <h2 className="text-3xl font-semibold text-yellow-300 mb-6">Roadmap</h2>
        <div className="grid gap-6 sm:grid-cols-2">
          {[
            { title: "Q2 2025", steps: ["Website Launch", "Whitepaper Release"] },
            { title: "Q3 2025", steps: ["Testnet Demo", "Community Airdrop"] },
            { title: "Q4 2025", steps: ["Mainnet Launch", "DEX Listing"] },
            { title: "2026", steps: ["Ecosystem Expansion", "DAO Governance"] }
          ].map(({ title, steps }, i) => (
            <Card key={i} className="bg-[#10163A] text-white">
              <CardContent className="p-4">
                <h3 className="text-xl font-bold text-yellow-400">{title}</h3>
                <ul className="list-disc list-inside text-sm mt-2 text-gray-300">
                  {steps.map((step, j) => <li key={j}>{step}</li>)}
                </ul>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      <footer className="mt-20 text-center text-sm text-gray-500">
        © 2025 nothing — Built on Solana | Hosted at: 
        <a href="https://nothing-solana.vercel.app" target="_blank" className="text-yellow-400 underline ml-1">
          nothing-solana.vercel.app
        </a>
      </footer>
    </main>
  );
}
