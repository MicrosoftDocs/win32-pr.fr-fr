---
title: Créer des animations
description: Créer des animations
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16c460908e7c782054a3f62ece87d01e7c9a817
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565749"
---
# <a name="creating-animations"></a>Créer des animations

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour commencer à créer des animations pour votre caractère, sélectionnez l’icône **animations** dans l’arborescence. La page **Propriétés** s’affiche avec les paramètres par défaut pour toutes les animations. Vous pouvez modifier la taille de trame, les paramètres de durée d’image par défaut et de palette de couleurs sur la page **Propriétés** .

### <a name="setting-your-characters-frame-size"></a>Définition de la taille du cadre du caractère

La hauteur et la largeur du frame d’animation doivent rester constantes dans toute la définition des caractères (c’est-à-dire, pour toutes les animations de ce caractère). Bien que vous puissiez modifier la taille de la trame à partir de sa valeur par défaut (128 x 128 pixels), les images affichées dans l’éditeur seront mises à l’échelle en fonction de la taille d’affichage par défaut. Si vous modifiez le paramètre frame par défaut, vous pouvez afficher la taille complète et non réduite du frame en choisissant **ouvrir la fenêtre frame** dans le menu **Edition** .

### <a name="setting-your-characters-palette"></a>Définition de la palette de votre caractère

Par défaut, l’éditeur utilise la première image bitmap que vous chargez pour définir la palette de couleurs par défaut de votre caractère, les couleurs qui déterminent le mode d’affichage du caractère et définit la couleur de la<sup>position 11 de</sup> la palette comme couleur de transparence. Toutefois, vous pouvez définir la palette et la transparence explicitement dans le groupe d' **informations palette** . Cela vous permet de spécifier un fichier image à utiliser pour la palette. Vous pouvez spécifier l’un des fichiers image d’animation ou n’importe quel fichier graphique. Le fichier de palette que vous spécifiez doit être un fichier de couleurs 8 bits (256). Une fois le chargement effectué, utilisez le bouton **modifier le paramètre** pour modifier la couleur de transparence.

La palette de couleurs de votre caractère ne doit pas remapper les couleurs système standard. L’éditeur réserve automatiquement la palette de couleurs du système lors de l’affichage des images. En outre, toutes vos images d’animation doivent utiliser la même palette de couleurs et la même couleur de transparence. C’est très important. Si ce n’est pas le cas, vous pouvez voir le remappage des couleurs de vos images lorsque vous les chargez dans l’éditeur.

Bien que vous puissiez définir la palette de couleurs pour le caractère, sur les systèmes Windows où les propriétés d’affichage sont définies sur une palette de couleurs 8 bits (256), la couleur du caractère sera soumise à la palette actuelle du système. Étant donné que les applications peuvent modifier la palette du système, le caractère peut ne pas s’afficher avec les paramètres de couleur appropriés. Bien qu’il n’existe aucun moyen d’éviter cela, vous pouvez réduire l’effet en limitant le nombre de couleurs que vous utilisez et en définissant la palette du caractère en fonction de la palette utilisée par l’application qui pilote le caractère. Par exemple, si vous développez un caractère à utiliser avec des pages Web, vous souhaiterez peut-être définir la palette de caractères à l’aide de la palette de demi-teintes de Microsoft Internet Explorer. Vous pouvez capturer la palette du navigateur en cliquant avec le bouton droit sur une image sur une page Web et en choisissant la commande **enregistrer l’image en tant que** et en choisissant **bitmap** dans l’option **type** de fichier, puis en cliquant sur **Enregistrer**. Pour optimiser vos fichiers image d’animation dans un fichier palette spécifique, vous pouvez utiliser un produit comme l’équilibre DeBabelizer.

### <a name="creating-a-new-animation"></a>Création d’une animation

Après avoir déterminé les paramètres globaux de votre animation, vous pouvez commencer à créer des animations. Pour créer une animation, choisissez **nouvelle animation** dans le menu **Edition** ou le bouton **nouvelle animation** de la barre d’outils. Cela ajoute une nouvelle icône d’animation dans l’arborescence sous l’icône **animations** et attribue un nom par défaut à la nouvelle icône. Vous pouvez renommer votre animation en tapant dans le champ nom de l' **animation** . Notez que les noms d’animation dans une définition de caractère doivent être uniques. Par ailleurs, évitez d’utiliser des caractères dans le nom qui ne sont pas des caractères valides pour les noms de fichiers.

### <a name="adding-frames"></a>Ajouter des frames

Chaque animation est composée de frames. Pour créer un nouveau Frame pour votre animation, choisissez **nouveau Frame** dans le menu **Edition** ou dans la barre d’outils. Cela ajoute une nouvelle icône de frame à l’arborescence sous votre icône d’animation et affiche trois pages à onglets. La page **général** comprend des contrôles qui vous permettent de charger et d’ajuster une image pour votre cadre. Il comprend également une zone d’affichage pour l’apparence du cadre.

![Capture d’écran montrant le nom du fichier, le chemin d’accès et la position du volet image.](images/f2charflame.gif)

Un frame peut contenir une ou plusieurs images. Pour définir une image pour un cadre, cliquez sur le bouton **Ajouter un fichier image** juste au-dessus de la zone de liste **images** . La boîte de dialogue **Sélectionner les fichiers image** s’affiche et vous permet de sélectionner un fichier image bitmap.

![Capture d’écran montrant la sélection d’un fichier image dans l’Explorateur de fichiers.](images/f3chardialbox.gif)

Sélectionnez le fichier que vous souhaitez charger, choisissez **ouvrir**, et l’image s’affiche dans l’affichage du cadre sur la page **général** . L’éditeur accepte les images stockées sous la forme d’un format bitmap 1 bit (monochrome), 4 bits ou 8 bits, ou au format GIF.

Vous pouvez utiliser les quatre boutons fléchés sous l’image dans la zone **position** pour ajuster l’apparence de l’image dans le cadre. Si l’image est plus grande que la taille de votre cadre, seule la partie de l’image qui apparaît dans le frame s’affiche. Si vous augmentez la taille du cadre, l’image peut être mise à l’échelle pour s’ajuster à la zone d’affichage de l’éditeur.

Vous pouvez également afficher un frame en choisissant **ouvrir la fenêtre frame** dans le menu **Edition** . Cela permet d’afficher le frame actuel dans une fenêtre distincte sans mettre à l’échelle les images chargées dans le frame. La taille initiale de cette fenêtre est basée sur les paramètres de hauteur et de largeur de votre image. Vous pouvez le redimensionner plus petit, mais pas plus grand. La fenêtre frame reflète les modifications que vous apportez à l’aide des contrôles dans l’éditeur et vous permet également d’afficher le frame lors de l’affichage de ses autres pages de propriétés.

![Capture d’écran montrant le volet position.](images/f4charposctrl.gif)

Vous pouvez composer un frame à partir de plusieurs images. Chaque fois que vous sélectionnez le bouton **Ajouter une image** et que vous choisissez une autre image, l’image est ajoutée à la liste et à la zone d’affichage de l’image. Vous pouvez également ajouter plusieurs images en sélectionnant plusieurs fichiers. Appuyez sur Maj ou CTRL tout en cliquant dans la boîte de dialogue **Sélectionner les fichiers image** , puis choisissez **ouvrir**. Les boutons **monter** et **descendre** au-dessus de la zone de liste **images** déplacent une image sélectionnée dans l’ordre d’affichage (ordre de plan) du cadre. Vous pouvez également déplacer des images en les faisant glisser dans la liste. Si vous sélectionnez une image dans la liste et que vous cliquez sur le bouton **supprimer** , une image est supprimée. Pour modifier une image que vous avez chargée dans un autre fichier image, vous pouvez cliquer sur le nom de fichier pour le modifier directement ou utiliser le bouton **...** (points de suspension) pour afficher la boîte de dialogue **Sélectionner les fichiers image** et sélectionner un autre fichier.

![Capture d’écran montrant le bouton de sélection.](images/f5charell.gif)

Vous pouvez utiliser la zone de texte **durée** pour définir la durée du cadre ; autrement dit, la durée pendant laquelle le frame sera affiché. Si un frame n’a pas d’image et de durée nulle, le frame n’est pas affiché lors de la lecture de l’animation.

Vous pouvez également spécifier un fichier d’effet sonore à lire lorsque le frame est affiché. Si vous envisagez de charger le caractère à partir d’un serveur Web, vous souhaiterez peut-être compresser le fichier d’effet sonore pour réduire le temps de chargement. Vous pouvez ensuite spécifier le fichier audio compressé dans l’éditeur de caractères de l’agent. En outre, évitez d’utiliser un effet sonore avec une durée plus longue que la durée de votre animation et, en particulier, d’éviter un effet sonore qui boucle, car les services d’animation Microsoft Agent n’envoient pas d’événement de fin d’animation tant que le son n’est pas terminé. Évitez également de spécifier un effet sonore pour les animations que vous attribuez aux États **écouteur** ou **audition** , car cela interfère avec les entrées vocales. Enfin, bien que vous puissiez inclure plusieurs effets sonores dans une animation, évitez de les placer pour qu’ils se chevauchent, car cela peut affecter le minutage de l’animation. En outre, gardez à l’esprit que les effets sonores peuvent jouer à des taux différents en fonction du matériel de l’utilisateur.

Pour ajouter des frames à votre animation, choisissez à nouveau la commande **nouveau Frame** et suivez la même procédure. En guise d’option, vous pouvez également charger plusieurs images et générer automatiquement de nouveaux frames pour eux. Pour utiliser cette fonctionnalité, choisissez **nouveaux frames à partir d’images** dans le menu **Edition** . Les frames sont créés dans l’ordre alphabétique en fonction des noms de fichiers d’image. Lorsque vous avez terminé de définir toutes les images pour votre animation, vous pouvez choisir la nouvelle commande d' **animation** pour commencer une nouvelle animation.

Il existe d’autres façons d’ajouter des frames aux animations et de déplacer des frames dans ou entre les animations. Vous pouvez sélectionner une autre image (de la même animation ou d’une autre) et choisir **couper** ou **copier**, puis sélectionner l’animation ou un cadre dans cette animation et choisir **coller**. Vous pouvez également faire glisser un cadre d’une animation à une autre. Si vous faites glisser dans une animation, l’action déplace le cadre. Si vous faites glisser vers une autre animation, elle copie le cadre. Le fait de faire glisser vers un frame précédent dans la même animation insère le cadre avant le frame vers lequel vous faites glisser. Le fait de faire glisser vers un frame suivant le place après le frame vers lequel vous faites glisser. Si vous faites glisser un frame à l’aide du bouton droit de la souris, le bouton relâcher affiche un menu contextuel avec vos options de transfert.

Vous pouvez également créer une animation en copiant une animation existante (sélectionnez l’animation et choisissez **copier**), puis en sélectionnant l’icône **animations** ou une autre icône d’animation et en choisissant **coller**. L’éditeur crée automatiquement un nouveau nom pour l’animation, même si vous pouvez modifier le nom.

### <a name="branching"></a>Création de branche

Lorsque vous créez un frame, vous pouvez également définir le cadre de la lecture suivante. Par défaut, le frame suivant joué dans la séquence d’animation est toujours le frame suivant dans l’ordre de plan. Toutefois, en choisissant la page création d’une **branche** , vous pouvez définir la probabilité pour un maximum de trois autres frames que le serveur peut lire. Entrez le pourcentage de probabilité et le numéro de frame cible dans les champs appropriés. Vous pouvez spécifier des branchements même pour les frames qui n’ont pas d’images et dont la durée est définie sur zéro. Cela vous permet de créer une branche sans afficher au préalable une image particulière.

![Capture d’écran montrant la page « branchement ».](images/f6charbranch.gif)

Vous pouvez utiliser la fonctionnalité de création de branche pour créer des animations qui s’exécuteront en boucle indéfiniment. Toutefois, Notez que lorsqu’une animation de bouclage est lue, les autres animations de la file d’attente du caractère ne sont pas lues tant qu’un événement (par exemple, un utilisateur qui appuie sur la touche Push-to-débats ou l’application cliente appelant la méthode Stop) n’a pas [**cessé**](stop-method.md) l’animation en boucle. Par conséquent, examinez attentivement le contexte dans lequel l’animation sera utilisée avant de créer une animation de bouclage.

La page création de branche vous permet également de créer des branchements de sortie. Une branche de sortie est une branche vers un frame que l’animation prendra lorsque l’animation sera arrêtée et avant la lecture de l’animation suivante. La définition des branches de sortie vous permet de vous déplacer sans heurts au cours de la transition d’une animation à une autre. Votre branchement de sortie ne doit pas créer de boucle circulaire, mais doit être en mesure de quitter la dernière image de l’animation.

Vous n’avez pas besoin de fournir une branche de sortie pour chaque frame. Toutefois, si vous ne le faites pas, l’animation suivra la branche normale du frame. Si le frame n’a pas de branche explicite, l’animation effectue automatiquement une branche vers le frame qui le suit. Par exemple, si vous branchez de l’image 3 à l’image 1 et que l’image 1 n’a pas d’autre branchement (branche normale ou de sortie), le frame 1 se branche au frame 2. Si le frame 2 n’a pas de branchement, l’animation rebranche au frame 3 et vous avez une boucle circulaire. Au lieu de cela, vous pouvez créer une branche du frame 3 à l’image 1, puis définir la branche de sortie de l’image 1 sur n’importe quelle image qui est après l’image 3 et qui passe normalement à la dernière image de l’animation.

Parfois, vous devrez peut-être créer une image finale explicite d’une animation qui n’est pas lue de façon visible, mais qui fournit une fin de l’animation. Par exemple, vous devez quitter l’animation, mais la sortie vers la dernière image n’est pas appropriée. Pour ce faire, vous pouvez créer un frame vide de durée zéro comme dernière image de l’animation. Cela permet à l’animation de s’exécuter normalement à travers la dernière image de l’animation et vous permet également de fournir un point de sortie final pour votre branche de sortie.

### <a name="previewing-an-animation"></a>Aperçu d’une animation

Vous pouvez afficher un aperçu de votre animation dans l’éditeur de caractères de l’agent en choisissant la commande **Aperçu** dans le menu **Edition** ou le bouton Aperçu dans la barre d’outils. Cela lit votre animation, y compris les branches et les effets sonores, en commençant par le cadre actuellement sélectionné. Elle est rétablie dans le frame sélectionné actuel lorsque l’animation est terminée. Pour lire l’intégralité de votre animation, accédez à l’arborescence, sélectionnez l’icône ou la première image de l’animation, puis choisissez la commande **Aperçu** . L’éditeur anime vos frames sur la page **général** . Pour arrêter la version préliminaire avant qu’elle ne se termine, choisissez la commande **arrêter l’aperçu** . La commande **Aperçu** est automatiquement remplacée par l’option **arrêter** l’aperçu pendant la lecture de la version préliminaire.

Vous pouvez également afficher un aperçu de votre branchement de sortie en choisissant la commande **Aperçu quitter la branche** dans le menu **Edition** ou dans la barre d’outils. Vous permet de tester la manière dont la branche de sortie s’affiche à partir de n’importe quel Frame spécifique.

### <a name="assigning-speaking-overlays"></a>Assigner des superpositions de parole

Vous pouvez définir un caractère afin qu’il intervient au cours de la dernière image de son animation. Sur ce cadre, choisissez la page **superposition** . Cette page vous permet de charger et d’affecter des fichiers d’image de bouche aux positions de bouche standard prises en charge par Microsoft Agent. Cliquez sur le bouton **Ajouter une image** , puis sélectionnez l’image dans la boîte de dialogue. Vous pouvez également sélectionner plusieurs images, et l’éditeur chargera et affectera les images à partir de la position de bouche que vous avez sélectionnée. Cliquez sur les boutons **monter** et **descendre** , ou faites glisser une entrée pour modifier l’affectation d’une image dans la liste. Cliquez sur le bouton **supprimer** pour supprimer une image. Vous pouvez également modifier le nom du chemin d’accès d’un fichier affecté en cliquant sur son entrée dans la liste et en retapant son nom de fichier, ou en choisissant le bouton de **sélection** pour afficher la boîte de dialogue **Sélectionner les fichiers image** .

![Capture d’écran montrant la page « superpositions » avec un fichier sélectionné.](images/f7charover.gif)

Vos superpositions de bouche doivent tenir dans le contour du frame de base sur lequel elles s’affichent. Si ce n’est pas le cas, elles sont découpées dans le frame de base.

Si vous souhaitez que le caractère parle d’une bouche en dehors du frame de base, par exemple, lorsque le caractère doit parler d’un côté latéral, commencez par créer le frame de base avec l’en-tête du caractère (ou la zone à déplacer comme le caractère dit) comme image du haut. Ensuite, définissez vos superpositions de bouche pour remplacer cette image et définissez l’option **remplacer l’image de base du frame de base** . Vous pouvez également utiliser le bouton **définir tout** pour définir cette option pour tous les superpositions de l’embouchure dans le cadre.

### <a name="assigning-a-return-animation"></a>Assignation d’une animation de retour

Pour créer une transition en douceur d’une animation à la suivante, concevez vos séquences d’animation de manière à ce qu’elles commencent et se terminent par une image neutre. Pour plus d’informations, consultez [**conception de caractères pour Microsoft Agent**](designing-characters-for-microsoft-agent.md). Toutefois, cela ne signifie pas que chaque animation doit se terminer à la position neutre. Vous pouvez animer un caractère à travers une séquence de frames, le faire parler au cours de la dernière image et créer une animation distincte et complémentaire qui retourne le caractère à la position neutre. Cette animation complémentaire est appelée animation de retour.

Vous pouvez définir une animation de retour en créant une animation explicite à cet effet. Vous pouvez également créer une animation de retour à l’aide de la branche de sortie que vous définissez dans l’animation. Pour affecter une animation de retour, sélectionnez l’animation dans l’arborescence, puis sélectionnez l’animation de retour que vous avez créée ou utilisez quitter la création de branche dans la liste déroulante animation de retour de la page Propriétés.

La création et l’affectation d’une animation de retour ont un avantage supplémentaire : lorsque le serveur reçoit une demande de lecture d’une autre animation, il tente de lire l’animation de retour pour la dernière animation qu’il a jouée, si une animation de retour est assignée. Cela garantit une transition sans heurts. Si une animation commence et se termine à la position neutre, vous n’avez pas besoin de définir une animation de retour. De même, si vous envisagez de gérer des transitions d’une animation à une autre, vous n’aurez peut-être pas besoin d’assigner une animation de retour.

### <a name="assigning-animations-to-states"></a>Assigner des animations aux États

Les services d’animation Microsoft Agent lisent automatiquement les animations lorsque l’application cliente d’hébergement utilise certaines méthodes. Par exemple, lorsqu’une application appelle les méthodes [**MoveTo**](moveto-method.md) et [**GestureAt**](gestureat-method.md) , le serveur détermine automatiquement l’emplacement d’affichage du caractère et exécute une animation appropriée. De même, Microsoft Agent lit automatiquement les animations inactives lorsque l’utilisateur n’a pas interagi avec le caractère pendant plusieurs secondes. Ces conditions, lorsque le serveur lit automatiquement les animations au nom d’une application, sont appelées *États*. Toutefois, pour que le serveur sache quelle animation lire, vous devez assigner des animations à ces États.

Pour assigner une animation ou des animations à un État, créez l’animation appropriée, développez l’entrée États dans l’arborescence de la fenêtre de l’éditeur, puis sélectionnez l’icône État. La liste des animations que vous avez créées s’affiche dans une zone de liste sur le côté droit de la fenêtre. Vérifiez l’animation que vous souhaitez affecter à cet État. Notez que vous pouvez assigner plusieurs animations au même État. Cela permet au serveur de sélectionner de manière aléatoire différentes animations pour l’État. L’affectation d’une animation à un État n’empêche pas une animation de la diffuser directement.

Vous pouvez également affecter une animation à un État en sélectionnant l’entrée de l’animation dans l’arborescence. La zone de liste **attribuer à l’État** de la page **Propriétés** répertorie les États. Activez la case à cocher de l’État auquel vous affectez l’animation.

L’éditeur ne prend pas en charge la création d’États supplémentaires, car les États s’appliquent uniquement aux situations où le serveur doit lire une animation automatiquement pour le compte de l’application cliente. Ainsi, il n’y a aucun avantage à définir votre propre État. Si nécessaire, vous pouvez lire n’importe quelle animation explicitement à l’aide de la méthode [**Play**](play-method.md) .

### <a name="saving-your-character-definition"></a>Enregistrement de votre définition de caractère

Vous pouvez enregistrer le fichier de définition de votre caractère en choisissant la commande **Enregistrer** dans le menu **fichier** ou le bouton **enregistrer la définition de caractère** dans la barre d’outils. Si vous souhaitez enregistrer le fichier de définition de caractères sous un nouveau nom, choisissez la commande **Enregistrer sous** dans le menu **fichier** . L’éditeur enregistre la définition modifiable d’un caractère en tant que définition de caractère d’agent (. ACD). Vous pouvez également modifier ce format de fichier texte auto-documenté avec la plupart des éditeurs de texte et des applications de traitement de texte.

### <a name="printing-your-character-definition"></a>Impression de la définition de caractère

Pour imprimer la définition de votre caractère, choisissez la commande **Imprimer** dans le menu **fichier** ou le bouton **Imprimer** dans la barre d’outils. Pour définir les propriétés de la sortie imprimée, choisissez la commande **mise en page** et choisissez vos paramètres avant de sélectionner la commande **Imprimer** .

### <a name="building-a-character"></a>Génération d’un caractère

Lorsque vous avez terminé de créer vos animations, le caractère et les images doivent être compilés dans un format spécial utilisé par Microsoft Agent pour charger ces données. Pour générer un caractère, sélectionnez la commande générer un caractère dans le menu **fichier** ou dans la barre d’outils. Si vous avez des modifications non enregistrées dans votre fichier de définition de caractères, l’éditeur enregistre le fichier de définition avant d’afficher la boîte de dialogue **créer un caractère** .

![Capture d’écran montrant la fenêtre caractère de génération avec un fichier sélectionné.](images/f8charbldg.gif)

L’éditeur de caractères de l’agent propose automatiquement un nom de fichier en fonction de votre nom de fichier de définition de caractères. La boîte de dialogue caractère de build comprend également une liste déroulante qui vous permet de choisir entre la génération du caractère comme un fichier de stockage unique (. ACS) ou en tant que fichiers multiples. Si vous choisissez ce dernier, l’éditeur génère un. Fichier ACF qui comprend les données du caractère et un. Fichier de CCN pour chaque animation que vous avez créée. Si vous envisagez d’installer et d’accéder à un caractère stocké sur le même ordinateur que votre application cliente, vous devez généralement choisir le format de fichier structuré unique. Ce format offre une installation facile et efficace, ainsi qu’un accès au caractère. Toutefois, si le caractère est accessible à partir d’un serveur Web à l’aide du protocole HTTP, générez votre caractère à l’aide de. Format de fichier ACF (individuel). Cette dernière structure de fichiers permet à un script de page Web de charger des fichiers d’animation individuels, en stockant les données dans le cache des fichiers du navigateur de l’utilisateur. Il fournit un accès plus efficace sur le Web, car les données d’animation peuvent être téléchargées en fonction des besoins plutôt que de demander à l’utilisateur d’attendre le téléchargement de l’ensemble des animations à un moment donné. En outre, étant donné que les données du caractère sont stockées dans le cache du navigateur, l’espace de fichier peut être récupéré automatiquement.

Bien que vous puissiez également télécharger des données de caractères (comme un seul fichier structuré ou plusieurs fichiers) à partir d’un serveur Web et les installer ailleurs sur l’ordinateur d’un utilisateur, une telle méthode nécessite des dispositions de sécurité pour le téléchargement et l’installation. Par conséquent, l’API de l’agent Microsoft n’inclut pas la prise en charge de l’installation téléchargeable d’un caractère, sauf dans le cache du navigateur. Toutefois, vous pouvez toujours prendre en charge ce scénario en créant votre propre contrôle d’installation et en le distribuant selon les conventions de sécurité appropriées. Pour plus d’informations, consultez le kit de développement logiciel (SDK) Microsoft Internet client.

L’option compresser vous permet de définir si les données caractères sont compressées. En règle générale, vous pouvez définir cette option pour compacter vos données de caractères, bien que la génération d’un caractère avec les données compactées prenne plus de temps.

Une fois que vous avez généré un caractère, les builds suivantes sont plus rapides si vous générez le caractère dans le même emplacement de répertoire. L’éditeur de caractères vérifie et copie automatiquement les fichiers qui n’ont pas été modifiés, puis RECOMPILE toutes les données qui ont été modifiées.

Si l’éditeur détecte des erreurs dans le fichier de caractères lors de la génération du caractère, il écrit les informations dans un fichier journal et affiche une boîte de message. Vous pouvez choisir d’afficher le fichier journal ou de l’ignorer et de le lire ultérieurement à l’aide d’un éditeur de texte. Toutefois, Notez que l’éditeur remplacera le fichier journal lors de la prochaine génération d’un fichier de caractères.

### <a name="editing-an-existing-character"></a>Modification d’un caractère existant

Pour modifier un caractère existant, choisissez **ouvrir** dans le menu **fichier** , sélectionnez le fichier de définition du caractère (. ACD) dans la boîte de dialogue résultante, puis choisissez Ouvrir. Le fichier est chargé dans l’éditeur. Notez que vous ne pouvez pas charger les fichiers de caractères compilés (. ACS,. ACF, ou. CCN) avec l’éditeur.

Étant donné que le fichier de définition du caractère (. ACD) est un fichier texte, vous pouvez également modifier la définition d’un caractère en ouvrant le fichier avec un éditeur de texte ou un programme de traitement de texte. Toutefois, lorsque vous effectuez vos modifications, veillez à enregistrer le fichier dans son format d’origine avant de le charger dans l’éditeur de caractères pour la compilation.

 

 




