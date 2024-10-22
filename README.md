# Checkpoint-Next-JS


Construire un site web de portfolio avec Next.js est un excellent projet pour mettre en pratique vos compétences. Voici un guide étape par étape pour vous aider à démarrer :

1. Mise en route avec Next.js
Initialiser le projet :

bash
Copier le code
npx create-next-app mon-portfolio
cd mon-portfolio
Structure du projet : Vérifiez que votre projet a la structure suivante :

arduino
Copier le code
mon-portfolio/
├── pages/
│   ├── index.js        // Page d'accueil
│   ├── about.js        // Page à propos
│   ├── projects.js      // Page des projets
│   └── contact.js       // Page de contact
├── components/          // Dossier pour vos composants réutilisables
├── public/              // Dossier pour les images et autres fichiers statiques
├── styles/              // Dossier pour les fichiers CSS
└── .next/               // Dossier créé lors du build (non à modifier)
2. Styler les composants et afficher les images
Styler avec des modules CSS : Créez un fichier CSS pour chaque page ou composant. Par exemple, styles/Home.module.css pour la page d'accueil.

css
Copier le code
/* styles/Home.module.css */
.container {
    padding: 20px;
    text-align: center;
}

.title {
    font-size: 2em;
    color: #333;
}
Afficher les images : Utilisez le composant Image de Next.js pour une gestion optimisée des images.

jsx
Copier le code
// pages/index.js
import Image from 'next/image';
import styles from '../styles/Home.module.css';

const Home = () => {
    return (
        <div className={styles.container}>
            <h1 className={styles.title}>Bienvenue sur mon Portfolio</h1>
            <Image src="/profile.jpg" alt="Mon Profil" width={150} height={150} />
        </div>
    );
};

export default Home;
3. Routage par page avec Next.js
Créer des pages : Ajoutez des fichiers pour chaque section de votre portfolio dans le dossier pages.

jsx
Copier le code
// pages/about.js
const About = () => {
    return <h2>À propos de moi</h2>;
};

export default About;

// pages/projects.js
const Projects = () => {
    return <h2>Mes Projets</h2>;
};

export default Projects;

// pages/contact.js
const Contact = () => {
    return <h2>Contactez-moi</h2>;
};

export default Contact;
Routage par fichier : Next.js gère automatiquement le routage en fonction de la structure des fichiers dans le dossier pages. Ainsi, /about correspondra à about.js, etc.

4. Déployer le site
Pour déployer votre application, vous pouvez utiliser Vercel, qui est la plateforme par défaut pour Next.js. Suivez ces étapes :

Installez Vercel CLI :

bash
Copier le code
npm i -g vercel
Déployez votre projet :

bash
Copier le code
vercel
Suivez les instructions : Choisissez votre compte et le projet sera déployé.

Conclusion
Vous aurez maintenant un site web de portfolio fonctionnel construit avec Next.js, comprenant plusieurs pages, un style personnalisé, et des images.
