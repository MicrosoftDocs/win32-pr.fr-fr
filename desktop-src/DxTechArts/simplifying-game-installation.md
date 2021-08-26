---
title: Simplification de l’installation du jeu
description: cet article décrit quelques concepts que les développeurs de jeux pour Windows peuvent et doivent implémenter pour améliorer l’expérience globale.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53062b9905e59435f1b9175eb95832294d93e51193003622d3bcc6dd16ee07df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042465"
---
# <a name="simplifying-game-installation"></a>Simplification de l’installation du jeu

l’un des principaux avantages des jeux qui s’exécutent sur une console au lieu de Windows est le processus d’installation, ou l’absence de ce dernier. Lorsqu’un jeu est exécuté pour la première fois sur une console, le lecteur effectue quelques choix ou confirmations et peut commencer à jouer presque immédiatement. l’installation d’un jeu sur Windows est plus complexe, par comparaison, par la nécessité d’une entrée utilisateur importante et de son processus d’installation potentiellement long. toutefois, ce processus d’installation peut être amélioré pour offrir une meilleure expérience aux joueurs de jeux basés sur Windows. cet article décrit quelques concepts que les développeurs de jeux pour Windows peuvent et doivent implémenter pour améliorer l’expérience globale.

-   [Installation classique de jeux](#typical-game-installation)
-   [Installation simplifiée des jeux](#simplified-game-installation)
    -   [Posez toutes les questions à l’avance](#ask-all-questions-up-front)
    -   [Fournir des modes d’installation spéciaux](#provide-special-installation-modes)
    -   [Réduire la quantité de questions sur l’installation](#minimize-the-quantity-of-installation-questions)
    -   [Modifier les composants facultatifs en composants requis](#change-optional-components-into-required-components)
    -   [Toujours installer DirectX et le faire en mode silencieux](#always-install-directx-and-do-so-silently)
    -   [Réfléchissez à votre CLUF](#think-about-your-eula)
    -   [Lancer automatiquement après l’installation](#automatically-launch-after-installation)
    -   [Optimiser les performances de votre installation](#optimize-your-installation-performance)
    -   [s’inscrire auprès d’Windows pare-feu pendant l’Installation](#register-with-windows-firewall-during-installation)
    -   [Installer pour tous les utilisateurs, pas seulement l’utilisateur actuel](#install-for-all-users-not-just-the-current-user)
-   [Exemple d’installation simplifiée](#example-of-simplified-installation)
-   [Résumé](#summary)

## <a name="typical-game-installation"></a>Installation classique de jeux

Lorsque vous comparez la facilité d’installation et la durée nécessaire pour commencer à jouer un jeu, l’expérience de la Xbox est bien meilleure que Windows. l’organigramme de la Figure 1 montre les processus d’installation typiques sur la Xbox et sur Windows, à des fins de comparaison.

**Figure 1. Processus d’installation par défaut, Xbox et Windows**

![Xbox \- vs \- PC](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Installation simplifiée des jeux

toutefois, les exigences supérieures imposées à l’utilisateur pour installer un jeu sur Windows n’ont pas besoin d’être. En implémentant les concepts suivants, vous allez réduire le nombre d’étapes qu’un utilisateur doit effectuer, ce qui peut raccourcir le temps nécessaire à l’installation.

### <a name="ask-all-questions-up-front"></a>Posez toutes les questions à l’avance

Tous les choix que les joueurs sélectionnent au cours de l’installation et qui peuvent entraîner l’abandon de l’installation doivent être proposés avant ceux qui n’arrêtent pas l’installation. dans le pire des cas, il est possible de proposer au joueur un choix pouvant entraîner l’abandon de l’installation une fois que le jeu a été entièrement copié à partir du support d’installation. Cela peut être particulièrement frustrant si l’installation nécessite l’échange de plusieurs disques pour se terminer. Vous devez concevoir votre programme d’installation pour qu’il pose toutes les questions importantes (telles que l’acceptation du CLUF) au début du processus, afin que l’installation n’ait pas besoin d’être restaurée à son achèvement ou à une approche proche.

Vous pouvez également inviter l’utilisateur à accepter le CLUF et à entrer la clé de produit au démarrage du jeu pour la première fois, au lieu de lui demander de le faire dans le cadre de l’installation. Dans ce scénario, le refus d’accepter le CLUF ou l’annulation lors de l’entrée de la clé de produit ne restaure pas l’installation, car ces invites font partie du jeu lui-même. Cela peut être utile si vous avez des scénarios préinstallés ou OEM. Toutefois, veillez à ne pas inviter l’utilisateur à effectuer des choix au cours du démarrage initial qui requièrent des informations d’identification d’administration.

### <a name="provide-special-installation-modes"></a>Fournir des modes d’installation spéciaux

dans l’idéal, Windows programmes d’installation de jeux ne doivent offrir que des modes d’installation entièrement automatiques et personnalisés, et rien d’autre.

Le mode automatique ne doit pas poser d’autres questions que nécessaire pour créer une installation fonctionnelle et utiliser simplement les paramètres par défaut sans demander d’autres options. De nombreux joueurs ne se soucient pas de l’emplacement du jeu sur le disque dur ou des paramètres de jeu initiaux, mais ils veulent simplement jouer le jeu le plus rapidement possible.

Le mode personnalisé doit uniquement être destiné aux utilisateurs avec pouvoir qui ont besoin de modifier le chemin d’installation ou d’autres options d’installation, et il ne doit pas être le mode par défaut.

Le mode personnalisé peut offrir le choix entre une installation complète ou une installation minimale qui installe uniquement les fichiers nécessaires pour jouer au jeu. Si le joueur choisit une installation minimale, le jeu peut utiliser des techniques d’installation à la demande ou de diffusion en continu pour lire les données d’installation restantes, ce qui permet aux joueurs de commencer à jouer rapidement le jeu sans devoir attendre la fin d’une installation complète. Toutefois, l’installation de données de cette manière a un impact sur la conception du moteur de jeu. Pour plus d’informations sur l’installation de contenu à la demande, consultez [installation à la demande pour les jeux](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Réduire la quantité de questions sur l’installation

Dans les deux modes d’installation, vous devez essayer de limiter le nombre de fois où vous invitez les joueurs pendant l’installation. Cela permet de réduire la quantité de lectures requises pour installer et exécuter le jeu. Si nécessaire, il ne doit y avoir qu’une seule invite de suivi une fois l’installation terminée. Comme vous pouvez le voir, l’exemple illustré à la figure 1 contient trop d’invites après l’installation.

### <a name="change-optional-components-into-required-components"></a>Modifier les composants facultatifs en composants requis

Procédez à l’installation de tous les composants requis au lieu de les rendre facultatifs, à moins qu’il y ait une bonne raison de le faire autrement. Le simple fait d’installer tous les composants permet de démarrer le jeu sans délai supplémentaire.

### <a name="always-install-directx-and-do-so-silently"></a>Toujours installer DirectX et le faire en mode silencieux

Il est fortement recommandé que le jeu installe sans assistance le package redistribuable DirectX sur lequel le jeu a été créé. Le processus d’installation de DirectX est conçu pour vérifier si quelque chose doit être mis à jour et retourne rapidement si ce n’est pas le cas. Par conséquent, il n’est pas nécessaire de demander aux utilisateurs s’ils souhaitent installer DirectX. Une installation sans assistance de DirectX peut être effectuée en exécutant cette commande à partir de votre package d’installation : **dxsetup.exe/Silent**

Demander à un utilisateur s’il souhaite installer DirectX peut entraîner de nombreux problèmes. Par exemple, si l’utilisateur suppose qu’il dispose du dernier redistribuable installé et qu’il choisit d’ignorer l’installation de DirectX ; l’installation du jeu peut se poursuivre avec succès. Toutefois, si le jeu requiert une version spécifique de D3DX ou d’autres fonctionnalités mises à jour qui ont été ignorées, le jeu ne fonctionnera pas et l’utilisateur sera très mécontent.

Si, pour une raison quelconque, vous devez demander à l’utilisateur s’il souhaite installer DirectX, votre programme d’installation doit, au moins, abandonner et annuler l’intégralité du processus d’installation si l’utilisateur choisit de ne pas installer DirectX. La restauration de l’installation évite toute erreur provoquée par le fait que le système n’a pas installé la dernière version de DirectX au lancement du jeu.

Notez qu’il est important d’expédier le package redistribuable sur lequel votre jeu a été créé au lieu d’envoyer simplement le package redistribuable à partir du dernier Kit de développement logiciel (SDK) DirectX. Le dernier redistribuable peut ne pas contenir tous les composants trouvés dans une version précédente.

Il est également important que le programme d’installation vérifie ce qui est déjà installé et détermine si le redémarrage du système est nécessaire. Si DirectX est à jour, la copie d’une DLL ne doit pas nécessiter un redémarrage.

### <a name="think-about-your-eula"></a>Réfléchissez à votre CLUF

Le CLUF DirectX peut et doit être ajouté au CLUF du développeur de jeux. Il n’y a aucun point dans la possibilité pour l’utilisateur d’accepter le CLUF du développeur et non le CLUF DirectX. Soit l’utilisateur doit accepter les deux CLUF, soit ne pas installer le jeu. Si un développeur pense qu’il doit proposer à l’utilisateur le choix, l’installation complète doit échouer si l’utilisateur choisit de ne pas accepter le CLUF DirectX.

Si possible, contactez votre service juridique pour savoir si vous pouvez éviter les CLUF entièrement et utiliser un CLUF en réduction comme les jeux de la console. Cela évite d’avoir à demander aux utilisateurs s’ils souhaitent accepter le CLUF. Le CLUF DirectX doit être ajouté au CLUF de réduction. dans le cas contraire, le CLUF DirectX doit être affiché et accepté, ce qui a pour effet d’utiliser un CLUF en réduction.

L’une des exceptions à un CLUF en réduction est l’éditeur de contenu. N’importe quel éditeur doit afficher un CLUF au cours de l’installation de l’éditeur ou lorsque l’éditeur est démarré pour la première fois. De nombreux joueurs sont uniquement intéressés par la création et non le contenu, donc l’installation d’un éditeur doit être un processus séparé.

### <a name="automatically-launch-after-installation"></a>Lancer automatiquement après l’installation

Presque tous les joueurs veulent jouer un jeu dès qu’ils le reçoivent. Par défaut, le programme d’installation doit lancer le jeu après la fin de l’installation, bien qu’il soit recommandé, dans une installation personnalisée, de le spécifier dans une case à cocher que l’utilisateur peut remplacer.

### <a name="optimize-your-installation-performance"></a>Optimiser les performances de votre installation

Les développeurs doivent tester leurs installations pour déterminer le temps nécessaire à l’installation. Les développeurs peuvent réduire le temps d’installation en utilisant la dernière version de leurs outils d’installation et en optimisant la disposition des données sur le support d’installation. La plupart des outils de création de DVD offrent des options d’optimisation de la disposition qui peuvent améliorer les temps d’installation sans augmenter la charge de travail de développement.

### <a name="register-with-windows-firewall-during-installation"></a>s’inscrire auprès d’Windows pare-feu pendant l’Installation

si votre jeu peut s’exécuter en tant que serveur ou que le modèle de mise en réseau du jeu est égal à égal, inscrivez votre jeu avec Windows pare-feu au moment de l’installation. Cela empêchera la boîte de dialogue de pare-feu de s’afficher au milieu du jeu quand l’utilisateur tente d’accéder au réseau. Si le jeu est un client pur, le programme d’installation ne doit pas ajouter le jeu à la liste des exceptions du pare-feu.

pour plus d’informations, consultez Windows pare-feu pour les développeurs de jeux.

### <a name="install-for-all-users-not-just-the-current-user"></a>Installer pour tous les utilisateurs, pas seulement l’utilisateur actuel

Par défaut, il suffit d’installer le jeu pour tous les utilisateurs. Cela permet à tout nouvel utilisateur du système de jouer au jeu sans avoir à l’installer pour eux. Si l’installation de tous les utilisateurs est tentée sur un compte d’utilisateur Least-Privileged, le programme d’installation échouera ou invitera l’utilisateur à entrer un mot de passe d’administrateur. Par conséquent, essayez de déterminer si le compte dispose des privilèges appropriés avant de proposer l’option d’installation pour tous les utilisateurs. Si l’utilisateur choisit d’installer le jeu pour l’utilisateur actuel uniquement, veillez à modifier le chemin d’installation à un emplacement dans le profil de l’utilisateur. Dans l’idéal, modifiez le chemin d’accès à un emplacement dans les données d’application non itinérantes (par exemple, un sous-répertoire de CSIDL \_ local \_ AppData).

## <a name="example-of-simplified-installation"></a>Exemple d’installation simplifiée

la Figure 2 ci-dessous est un exemple de processus amélioré pour l’installation d’un jeu dans Windows, avec des boîtes de dialogue d’installation simplifiées.

**Figure 2. Processus d’installation simplifié**

![installer](images/simplifiedgameinstall.png)

Les points importants de la note sont les suivants :

-   Le programme d’installation est automatiquement lancé lors de l’insertion du disque d’installation (exécution automatique).
-   L’écran de démarrage, avec les options d’installation, de suppression, d’affichage du site Web ou de sortie, n’est pas affiché si le jeu n’est pas encore installé sur l’ordinateur.
-   La boîte de dialogue d' **installation** est la première de la boîte de dialogue affichée par le programme d’installation.
-   Le bouton **installer** correspond à l’implémentation du mode d’installation automatique.
-   Le bouton **options** est l’implémentation du mode d’installation personnalisée.
-   Le bouton **Annuler** va immédiatement quitter le programme d’installation. Étant donné que le lancement du programme d’installation est une action simple pour l’utilisateur, ne pas demander de confirmation.
-   Une fois que l’utilisateur a accepté le CLUF et entre une clé de produit valide, l’installation démarre.
-   Une fois le processus d’installation terminé, le jeu démarre automatiquement ou affiche une boîte de dialogue qui avertit l’utilisateur que l’installation est terminée et offre d’autres options, selon que l’option **exécuter le jeu après l’installation** a été sélectionnée.
-   La case à cocher **exécuter le jeu** offre une autre chance de lancer le jeu, pour des raisons pratiques. Cette option est toujours désactivée par défaut, car la boîte de dialogue **installation terminée** ne peut être affichée que si **exécuter le jeu après l’installation** n’a pas été sélectionné dans la boîte de dialogue **options d’installation** .
-   Le bouton **OK** ferme la boîte de dialogue, en effectuant éventuellement une action sur l' **exécution** et affiche les cases à cocher **du fichier Lisez-moi** .

## <a name="summary"></a>Résumé

Les joueurs veulent jouer un jeu le plus rapidement possible. La dernière chose qu’un joueur souhaite faire est de frayer par le biais de boîtes de dialogue et de faire des choix qui sont les mêmes que pour tous les autres jeux qu’il ou elle a installés. l’implémentation de ces idées peut raccourcir le temps passé par un joueur à installer un jeu sur Windows et à améliorer la qualité globale de l’expérience de jeux Windows.

 

 