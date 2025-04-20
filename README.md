import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function Home() {
  return (
    <main className="min-h-screen bg-white text-gray-800">
      <header className="bg-black text-gold p-6 flex justify-between items-center shadow-lg">
        <div className="flex items-center gap-4">
          <img src="/dalet-logo.png" alt="Dalet Symbol" className="h-12 w-auto" />
          <h1 className="text-2xl font-bold text-gold">Dalet Cleaning Services</h1>
        </div>
        <nav className="space-x-4">
          <a href="#services" className="text-gold hover:underline">Services</a>
          <a href="#about" className="text-gold hover:underline">About Us</a>
          <a href="#contact" className="text-gold hover:underline">Contact</a>
        </nav>
      </header>

      <section className="text-center py-16 px-6 bg-gradient-to-b from-gold to-white">
        <motion.h2 initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 1 }}
          className="text-4xl font-bold mb-4">
          Professional Cleaning for Homes and Offices
        </motion.h2>
        <p className="text-lg mb-6">Serving with excellence, integrity, and a golden touch.</p>
        <Button className="bg-gold text-black text-lg px-6 py-2 rounded-xl shadow hover:bg-yellow-400">
          Get a Free Quote
        </Button>
      </section>

      <section id="services" className="grid grid-cols-1 md:grid-cols-3 gap-6 px-6 py-12">
        <Card className="rounded-2xl shadow-xl p-6">
          <CardContent>
            <h3 className="text-xl font-semibold mb-2">Residential Cleaning</h3>
            <p>Keep your home spotless with our personalized cleaning plans.</p>
          </CardContent>
        </Card>
        <Card className="rounded-2xl shadow-xl p-6">
          <CardContent>
            <h3 className="text-xl font-semibold mb-2">Office Cleaning</h3>
            <p>Maintain a professional and sanitary workspace with scheduled services.</p>
          </CardContent>
        </Card>
        <Card className="rounded-2xl shadow-xl p-6">
          <CardContent>
            <h3 className="text-xl font-semibold mb-2">Deep Cleaning</h3>
            <p>Thorough cleaning services for special occasions or seasonal resets.</p>
          </CardContent>
        </Card>
      </section>

      <section id="about" className="px-6 py-12 bg-gray-100 text-center">
        <h2 className="text-3xl font-bold mb-4">Why Choose Dalet?</h2>
        <p className="max-w-2xl mx-auto">
          Dalet Cleaning Services is inspired by the Hebrew symbol "Dalet," representing a door — we open the door to purity and positive energy. Our team is dedicated to offering reliable, detail-oriented, and top-quality cleaning for homes and offices across the U.S.
        </p>
      </section>

      <section id="contact" className="px-6 py-12 text-center">
        <h2 className="text-3xl font-bold mb-4">Get In Touch</h2>
        <p className="mb-4">Ready to experience the golden standard of cleaning? Reach out today!</p>
        <form className="max-w-xl mx-auto grid gap-4">
          <input type="text" placeholder="Full Name" className="border p-3 rounded-xl" />
          <input type="email" placeholder="Email Address" className="border p-3 rounded-xl" />
          <textarea placeholder="Your Message" rows="4" className="border p-3 rounded-xl"></textarea>
          <Button className="bg-gold text-black text-lg px-6 py-2 rounded-xl shadow hover:bg-yellow-400">
            Send Message
          </Button>
        </form>
      </section>

      <footer className="bg-black text-gold text-center py-6 mt-12">
        <p>&copy; {new Date().getFullYear()} Dalet Cleaning Services. All rights reserved.</p>
      </footer>
    </main>
  );
}

const gold = "#FFD700";

const style = document.createElement("style");
style.innerHTML = `
  .text-gold { color: ${gold}; }
  .bg-gold { background-color: ${gold}; }
`;
document.head.appendChild(style);
