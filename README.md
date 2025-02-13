import { motion } from "framer-motion";
import { FaGithub, FaLinkedin, FaEnvelope } from "react-icons/fa";

export default function Profile() {
  return (
    <div className="bg-gray-900 text-white min-h-screen flex flex-col items-center p-8 space-y-8">
      {/* Header Animation */}
      <motion.h1
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 1 }}
        className="text-4xl font-extrabold text-center"
      >
        🚀 Hi, I'm <span className="text-blue-400">Sarfraz Ahmad</span>
      </motion.h1>
      <motion.p
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ delay: 0.5, duration: 1 }}
        className="text-lg text-center max-w-3xl"
      >
        A Full-Stack Developer, UI/UX Designer & Creative Thinker bringing ideas to life with smooth designs and robust applications.
      </motion.p>

      {/* Skill Cards with Hover Animation */}
      <div className="grid grid-cols-2 md:grid-cols-4 gap-6">
        {[
          "React", "Next.js", "TypeScript", "TailwindCSS", "Figma", "Adobe XD", "Git", "Sanity CMS"
        ].map((skill, index) => (
          <motion.div
            key={index}
            whileHover={{ scale: 1.1 }}
            transition={{ type: "spring", stiffness: 300 }}
            className="bg-gray-800 p-4 rounded-xl text-center font-semibold shadow-lg"
          >
            {skill}
          </motion.div>
        ))}
      </div>

      {/* Featured Projects Section */}
      <motion.div className="w-full max-w-4xl text-center">
        <motion.h2
          initial={{ opacity: 0, y: 50 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 1 }}
          className="text-2xl font-bold"
        >
          🔥 Featured Projects
        </motion.h2>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6 mt-4">
          {["E-commerce Platform", "UI/UX Design Portfolio", "Modern Portfolio"].map((project, i) => (
            <motion.div
              key={i}
              whileHover={{ scale: 1.05 }}
              className="bg-gray-800 p-6 rounded-lg shadow-lg"
            >
              <h3 className="text-lg font-semibold">{project}</h3>
              <p className="text-sm text-gray-400">A sleek and modern {project.toLowerCase()} built with cutting-edge tech.</p>
            </motion.div>
          ))}
        </div>
      </motion.div>

      {/* Contact Section */}
      <motion.div
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ delay: 1 }}
        className="flex space-x-6 text-xl"
      >
        <a href="https://github.com/creativesar" target="_blank" className="hover:text-blue-400 transition">
          <FaGithub />
        </a>
        <a href="https://www.linkedin.com/in/sarfraz-ahmad-595428286/" target="_blank" className="hover:text-blue-400 transition">
          <FaLinkedin />
        </a>
        <a href="mailto:uniqueluck68@gmail.com" className="hover:text-blue-400 transition">
          <FaEnvelope />
        </a>
      </motion.div>
    </div>
  );
}
