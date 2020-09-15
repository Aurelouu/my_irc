# my_irc

Introduction_ _ _ _ _ __ _ _ _ _Il s’agit dans ce projet de réaliser un serveur IRC grâce à NodeJS.Votre serveur devra accepter plusieurs connexions simultanées.Votre serveur devra implémenter la notion de “channels”.Il doit être possible de rejoindre plusieurs “channels” simultanément (Par exemple via un système d’onglet).

Restrictions_ _ _ _ _ __ _ _ _ _Pour ce projet, vous devez utiliser, et n’utiliser que :•node.js (node)•socket.io (web sockets et rooms)•express.js (node)•react.js (moteur de template js)

Cahier des charges_ _ _ _ _ __ _ _ _ _
+ Gestion des utilisateurs_ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _•Un système de connexion : l’utilisateur de votre site doit pouvoir se connecter en fournissant un nomd’utilisateur.•Tous les membres peuvent modifier leurs informations et ajouter des channels.•Le membre qui aura créé son channel pourra le supprimer et le modifier.

+ Gestion des channels_ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _•Chaque action (création et suppression) sur les channels et changement de pseudo enverra un mes-sage global visible sur tous les channels.•Un nouvel utilisateur se connectant à un channel devra envoyer un message visible sur ce channel.•Un channel devra s’auto supprimer si personne n’y a écrit depuis 2 jours (pour la soutenance mettre5 minutes).•Les membres connectés à un channel devront pouvoir envoyer un message à tous les utilisateurs dece channel, et seulement à celui-ci.•Le serveur devra maintenir à jour la liste des utilisateurs connectés (les sockets) ainsi que des channels(avec la listes des personnes connectées).

+ Commandes_ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _•/nicknickname: définit le surnom de l’utilisateur au sein du serveur.•/list[string]: liste les channels disponibles sur le serveur. N’affiche que les channels contenant lachaîne “string” si celle-ci est spécifiée.•/createchannel: créer un channel sur le serveur.•/deletechannel: suppression du channel sur le serveur.•/joinchannel: rejoint un channel sur le serveur.•/partchannel: quitte le channel.•/users: liste les utilisateurs connectés au channel.•/msgnickname message: envoie un message à un utilisateur spécifique.•message: envoie un message à tous les utilisateurs connectés au channel.L’envoi des messages se fait obligatoirement en tapant sur entrée, donc pas de saut à la ligne.

+ Front_ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _Ajouter une interface intuitive et responsive en REACT afin que l’utilisateur puisse utiliser le serveur IRC sansavoir à connaître les commandes du mode terminal.

Bonus_ _ _ _ _ __ _ _ _ _Vous êtes libre de faire les bonus que vous souhaitez.Par Exemple :•BBcode pour les messages•Emojis dans les messages•Autocompletion des commandes, channels, users•Autolink des #channels et des @usernames•Ctrl + entrée pour retour à la ligne dans un message•Respecter la RFC1459•Créer une BDD (avec Mongo par exemple, mais pas obligatoire) afin de sauvegarder toutes les in-formations nécessaires pour conserver les channels existants, les informations sur les utilisateurs quiutilisent le service et toutes autres informations qui vous sembleraient nécessaires.
