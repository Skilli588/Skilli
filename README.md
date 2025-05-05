import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Github, Linkedin, Mail, Globe } from "lucide-react"; import { motion } from "framer-motion";

export default function Portfolio() { return ( <main className="min-h-screen bg-gradient-to-br from-white to-gray-100 text-gray-900 px-6 py-10"> <section className="max-w-5xl mx-auto text-center space-y-8"> <motion.h1 className="text-5xl font-extrabold tracking-tight" initial={{ opacity: 0, y: -50 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }} > Hi, I'm Skilli — Web Developer & Designer </motion.h1>

<motion.p
      className="text-xl text-gray-600 max-w-2xl mx-auto"
      initial={{ opacity: 0 }}
      animate={{ opacity: 1 }}
      transition={{ delay: 0.3, duration: 0.6 }}
    >
      I craft beautiful, fast, and accessible digital experiences. Peace and love.
    </motion.p>

    <motion.div
      className="flex justify-center flex-wrap gap-4"
      initial={{ opacity: 0 }}
      animate={{ opacity: 1 }}
      transition={{ delay: 0.5, duration: 0.6 }}
    >
      <Button variant="outline" asChild>
        <a href="https://github.com/yourusername" target="_blank">
          <Github className="mr-2" /> GitHub
        </a>
      </Button>
      <Button variant="outline" asChild>
        <a href="https://linkedin.com/in/yourusername" target="_blank">
          <Linkedin className="mr-2" /> LinkedIn
        </a>
      </Button>
      <Button variant="outline" asChild>
        <a href="mailto:kingbullet588@gmail.com">
          <Mail className="mr-2" /> Email
        </a>
      </Button>
      <Button variant="outline" asChild>
        <a href="https://yourwebsite.com" target="_blank">
          <Globe className="mr-2" /> Website
        </a>
      </Button>
    </motion.div>
  </section>

  <section className="mt-16 max-w-5xl mx-auto">
    <h2 className="text-3xl font-bold mb-6 text-center">Featured Projects</h2>
    <div className="grid gap-6 md:grid-cols-2">
      {[1, 2, 3, 4].map((id) => (
        <motion.div
          key={id}
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ delay: id * 0.2, duration: 0.5 }}
        >
          <Card className="hover:shadow-xl transition-shadow border border-gray-200">
            <CardContent className="p-6 space-y-3">
              <h3 className="text-2xl font-semibold">Project Title {id}</h3>
              <p className="text-gray-600 text-sm">
                This project demonstrates advanced UI/UX and optimized performance using React, TailwindCSS, and modern dev practices.
              </p>
              <Button variant="link" className="p-0" asChild>
                <a href="#" target="_blank">View Project</a>
              </Button>
            </CardContent>
          </Card>
        </motion.div>
      ))}
    </div>
  </section>
</main>

); }

