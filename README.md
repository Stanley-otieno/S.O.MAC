# S.O.MACnpx create-react-app my-portfolio
cd my-portfolio
npm install -D tailwindcss
npx tailwindcss init
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
@tailwind base;
@tailwind components;
@tailwind utilities;
import React from 'react';

const Header = () => {
  return (
    <header className="bg-gray-800 text-white p-4">
      <h1 className="text-3xl">My Portfolio</h1>
    </header>
  );
};

export default Header;
import React from 'react';

const About = () => {
  return (
    <section className="p-4">
      <h2 className="text-2xl">About Me</h2>
      <p>I am an experienced software engineer with expertise in...</p>
    </section>
  );
};

export default About;
import React from 'react';

const projects = [
  { name: 'Project One', description: 'Description of project one.' },
  { name: 'Project Two', description: 'Description of project two.' },
];

const Projects = () => {
  return (
    <section className="p-4">
      <h2 className="text-2xl">Projects</h2>
      <ul>
        {projects.map((project, index) => (
          <li key={index} className="mb-2">
            <h3 className="text-xl">{project.name}</h3>
            <p>{project.description}</p>
          </li>
        ))}
      </ul>
    </section>
  );
};

export default Projects;
import React from 'react';

const Contact = () => {
  return (
    <section className="p-4">
      <h2 className="text-2xl">Contact</h2>
      <p>Email: example@example.com</p>
    </section>
  );
};

export default Contact;
import React from 'react';
import Header from './components/Header';
import About from './components/About';
import Projects from './components/Projects';
import Contact from './components/Contact';

const App = () => {
  return (
    <div className="App">
      <Header />
      <main>
        <About />
        <Projects />
        <Contact />
      </main>
    </div>
  );
};

export default App;
npm start
