---
title: Son
description: Le son est l’élément audio de l’expérience utilisateur.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 035f718494e5a0548324f3c5449c5e3ac3f49fa1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444540"
---
# <a name="sound"></a>Son

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Le *son* est l’élément audio de l’expérience utilisateur. Lorsqu’ils sont utilisés de manière appropriée, le son peut être une forme efficace de communication qui établit une relation non orale et même émotionnelle avec vos utilisateurs. Les sons peuvent être utilisés seuls ou en complément de l’interface utilisateur visuelle. Par exemple, l’ajout d’un effet sonore à une notification augmente la probabilité qu’il soit remarqué, en particulier si l’utilisateur ne regarde pas l’écran lorsqu’un événement se produit.

![capture d’écran de la boîte de dialogue de son ](images/vis-sound-image1.png)

À partir de l’onglet sons de l’élément du panneau de configuration du son, les utilisateurs peuvent apporter des modifications à leurs sons système.

Cet article traite de l’utilisation des sons dans un programme en réponse aux événements et aux actions des utilisateurs, et de l’intégration du contrôle sonore d’un programme à Windows. Elle ne couvre pas l’utilisation de la musique ou de la parole.

**Remarque :** Les instructions relatives aux [notifications](mess-notif.md) et à la [personnalisation](exper-branding.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

Pour déterminer si vous devez utiliser le son, posez-vous les questions suivantes :

-   **Existe-t-il un avantage évident pour l’utilisation du son ?** Étant donné que les inconvénients de l’utilisation du son peuvent facilement contrebalancer les avantages, utilisez le son uniquement lorsqu’il existe un avantage évident.
-   **L’utilisation du son est-elle appropriée ?** L’utilisation du son attire-t-elle sur les éléments qui sont dignes d’attention ? Les utilisateurs seraient-ils manqués du son s’ils étaient absents ? Concentrez-vous sur les sons qui tiennent les utilisateurs informés, qui seront susceptibles de modifier leur comportement ou de fournir des commentaires utiles.
-   **L’utilisation du son est-elle gênante ?** Y a-t-il des sons fréquents, forts et transférerez ? Les utilisateurs risquent-ils de réduire le volume système ou le volume de votre programme en raison de votre utilisation du son ?
-   **Utilisez-vous le son comme forme de communication principale ?** Dans de nombreux cas, comme pour les utilisateurs qui ont un certain niveau de perte auditive, le son ne doit pas être utilisé comme moyen de communication principal. Le son est plus efficace en complément d’autres moyens de communication (tels que du texte ou des éléments visuels).
-   **Les principaux utilisateurs ciblent-ils les professionnels de l’informatique ?** Le son est généralement inefficace pour les tâches destinées aux professionnels de l’informatique, car la plupart de leurs tâches s’exécutent sans assistance. En outre, le son n’est pas mis à l’échelle, Imaginez l’exécution de centaines de tâches à la fois et l’obtention de sons lorsqu’ils se terminent ou échouent.

## <a name="design-concepts"></a>Principes de conception

En général, le son réalise une ou plusieurs des opérations suivantes :

-   **Notification.** Le son peut être associé à des événements spécifiques. Par exemple, un son « nouveau message » indique aux utilisateurs quand le courrier arrive sans interrompre la tâche en cours.
-   **Commentaires.** Le son peut fournir des commentaires pour des actions spécifiques de l’utilisateur. Par exemple, un son subtil qui s’exécute lorsque vous relâchez le curseur sur le contrôle du volume fournit des commentaires sur le niveau du paramètre actuel.
-   **Personnalisation.** Le son peut être associé à du contenu spécifique pour la personnalisation de votre produit, de votre application ou de votre service. Windows utilise le son de cette façon pour le démarrage du système d’exploitation.
-   **Diverti.** Le son est couramment utilisé pour améliorer les produits de divertissement et pour rendre tout produit plus attrayant. Par exemple, la plupart des jeux, des applications de formation et des produits grand public utilisent du son pour divertir les utilisateurs et améliorer leur expérience.

Certains sons peuvent satisfaire simultanément à plusieurs de ces objectifs. Le son de démarrage de Windows, par exemple, indique que le processus de démarrage est terminé et que le bureau est prêt à être utilisé. Il fournit également une forme puissante de la personnalisation des produits et, même momentanément, il s’agit d’un utilisateur.

Les sons qui ne remplissent aucun de ces objectifs doivent probablement être éliminés.

### <a name="inappropriate-use-of-sound"></a>Utilisation inappropriée du son

**Malgré les avantages du son, l’utilisation appropriée du son nécessite une restriction importante, sinon peut rendre un programme ennuyeux et gênant.** Les utilisateurs désactiveront leur son complètement s’ils sont importunés par des sons fréquents, répétitifs, transférerezs, perturbés, des sons mal conçus ; en partie, cela est dû au fait que sa nature, le bruit exige une attention et est difficile à ignorer. Pour obtenir des conseils sur la recherche d’un solde raisonnable, consultez les [instructions de conception audio](#sound-design).

Étant donné que les inconvénients de l’utilisation du son peuvent facilement contrebalancer les avantages, utilisez le son uniquement lorsqu’il existe un avantage évident. **En cas de doute, n’utilisez pas de son.**

### <a name="make-sound-supplemental"></a>Rendre le son plus complet

Même si le son est utilisé de manière appropriée, il existe de nombreuses situations où le son peut ne pas être efficace pour tous les utilisateurs :

-   Certains utilisateurs peuvent travailler dans un environnement bruyant où les sons ne peuvent pas être audibles.
-   Certains utilisateurs peuvent travailler dans un environnement silencieux qui requiert que le son soit désactivé ou défini sur un volume faible.
-   Certains utilisateurs peuvent avoir des troubles de l’audition ou une perte.
-   L’ordinateur ne dispose peut-être pas de haut-parleur.

Pour ces raisons, **le son utilisé pour les notifications et les commentaires ne doit jamais être la seule méthode de communication,** mais plutôt des indications visuelles ou textuelles.

### <a name="desirable-characteristics-of-sound"></a>Caractéristiques souhaitables du son

En général, les sons doivent être :

-   fréquence moyenne à haute (600 Hertz \[ Hz \] à 2 kilohertz \[ kHz \] ).
-   short (moins d’une seconde).
-   faible ou modéré en volume.
-   véritable.
-   agréable, sans alarme ou transférerez.
-   non verbal.
-   non répétitif.

Avec le son, moins est plus grand. **L’effet sonore idéal est celui que les utilisateurs remarquent à peine, mais ils manquent s’ils étaient absents.**

**Une fausse idée est que les sons pour les événements critiques doivent être forts et transférerez pour attirer l’attention de l’utilisateur.** Ce n’est pas vrai, car le son est vraiment destiné à être un moyen supplémentaire de communication. Dans le cas d’un message d’erreur critique, sa présentation (peut-être dans une boîte de dialogue modale), son icône (icône d’erreur) et son texte et son caractère de ton sont combinés pour communiquer la nature de l’erreur. Un son d’erreur efficace peut être légèrement plus élevé que le son habituel de Windows, mais il n’est pas nécessaire d’être beaucoup plus fort.

### <a name="characteristics-of-windows-sounds"></a>Caractéristiques des sons Windows

Au-delà de cet appel général pour le minimumisme, le son esthétique de Windows utilise des tonalités légères, pures et des sons en verre et Airy, avec un fondu souple et un fondu (« bords » adoucis) pour éviter les effets brusques, transférerezs et à percussion. Elles sont conçues pour paraître subtiles, légères et consonnes. Les sons Windows utilisent l’écho, la réverbération et l’égalisation pour atteindre un sentiment naturel et ambiant.

Le modèle de son par défaut pour Windows n’utilise généralement pas les sons quotidiens Instrumentals ou reconnaissables qui sont trop spécifiques ou musicaux. Des exemples de sons évités sont des instruments de musique tels que des pianos ou des instruments à percussion, des sons d’animaux, des bruits environnementaux, des voix, des voix, des effets sonores cinématographiques ou d’autres sons d’êtres humains. En outre, les sons Windows ne sont pas censés être perçus comme de la musique (autrement dit, Melodies). Cela rend les sons Windows fonctionnellement distincts des autres types de sons.

Étant donné que les sons Windows ont été conçus par des professionnels pour avoir les caractéristiques et les attraits souhaitables pour un large public, **envisagez d’utiliser ces sons Windows intégrés quand cela est approprié.**

### <a name="designing-your-own-sounds"></a>Conception de vos propres sons

Si vous devez créer vos propres sons, concevez-les pour qu’ils présentent les caractéristiques décrites précédemment. Efforcez-vous de compléter leurs tâches ou événements associés.

Sachez qu’il est difficile de créer des sons originaux particulièrement pour les sons destinés à un large public. Le son peut être un élément de conception polarisant. Pour chaque utilisateur qui aime un son, il y aura beaucoup qui l’aime.

**Concevez les sons de votre programme en tant que groupe pour qu’ils ressemblent à des variantes associées sur un thème.** L’expérience d’audit de votre programme doit être coordonnée avec son expérience visuelle. En outre, la « tonalité » des sons doit être coordonnée avec la [tonalité du texte](text-style-tone.md). Réfléchissez à la façon dont le texte avec un ton agréable et naturel peut être sous-compromis lorsqu’il est accompagné de sons difficiles, alarme.

**Si vous ne faites que quatre choses...**

1.  Utilisez le son avec une contrainte pour vous assurer qu’il existe un avantage global pour l’utilisateur. En cas de doute, n’utilisez pas de son.
2.  Utilisez les sons Windows intégrés quand cela est approprié.
3.  Si vous concevez vos propres sons, assurez-vous qu’ils présentent les caractéristiques sonores souhaitées et qu’il s’agit d’une apparence complète comme les variantes d’un thème.
4.  Ne partez pas du principe que les sons doivent être forts et transférerez pour attirer l’attention de l’utilisateur.

## <a name="usage-patterns"></a>Modèles d’usage

Les sons ont plusieurs modèles d’utilisation :



|     Utilisation du son                                                                                                                                                                 |  Exemple                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Achèvement de l’action**<br/> avertit les utilisateurs quand une action lancée à long terme par l’utilisateur se termine avec succès. <br/>                             | ![capture d’écran de la boîte de dialogue de téléchargement de fichier ](images/vis-sound-image2.png)<br/> Dans cet exemple, la boîte de dialogue émet un son pour avertir les utilisateurs que le téléchargement est terminé.<br/>                                                                                                                                                                                                                                      |
| **Échec de l’action**<br/> avertit les utilisateurs de façon Sonic quand une action lancée à long terme par l’utilisateur échoue. <br/>                                                 | ![capture d’écran du message d’inaccessibilité du disque de sauvegarde ](images/vis-sound-image3.png)<br/> Dans cet exemple, Windows émet un son pour avertir les utilisateurs que l’opération de sauvegarde a échoué.<br/>                                                                                                                                                                                                                                  |
| **Événement système important**<br/> avertit de façon Sonic les utilisateurs d’événements système importants ou de l’État qui requièrent une attention immédiate. <br/>                      | ![capture d’écran d’un message de batterie faible ](images/vis-sound-image4.png)<br/> Dans cet exemple, les utilisateurs sont avertis que leur batterie faible requiert une attention immédiate.<br/>                                                                                                                                                                                                                                                      |
| **INFORMATION**<br/> avertit les utilisateurs des informations pertinentes potentiellement utiles. <br/>                                                                 | Étant donné que ces informations ne nécessitent généralement pas une attention immédiate, un signal sonore fournit des commentaires subtils sans rompre le Flow de l’utilisateur. <br/> ![capture d’écran du message de connexion à Live Messenger ](images/vis-sound-image5.png)<br/> Dans cet exemple, un son est lu lorsqu’un contact se connecte à un service de messagerie instantanée.<br/>                                                                                 |
| **Effet sonore**<br/> Sonic fournit des commentaires aux interactions de l’utilisateur. <br/>                                                                            | Fournit des commentaires sur les sons réels ou stylisés qui sont appropriés pour l’interaction. les effets sonores sont souvent sonores comme si l’utilisateur manipule un objet physique réel. parfois appelé Foley. <br/> ![capture d’écran de la fenêtre réduite ](images/vis-sound-image6.png)<br/> Dans cet exemple, l’effet sonore de la fenêtre réduire ressemble à un objet réel dont la taille est réduite.<br/> |
| **Personnalisation des sons**<br/> son fourni pour améliorer l’expérience utilisateur en dépit de son impact émotionnelle et, en tant qu’effet secondaire, promouvoir la gamme de produits. <br/> | Les sons de personnalisation sont préférables lorsqu’ils sont synchronisés avec des événements visuels, en particulier des transitions d’interface utilisateur telles que l’affichage d’une fenêtre de programme. les marques de son vrai indiquent la source des marchandises, comme le mot ou le logo d’une marque, et sont relativement rares. <br/> ![capture d’écran de l’icône de démarrage de Windows ](images/vis-sound-image7.png)<br/> Dans cet exemple, le démarrage de Windows est une expérience de transition personnalisée.<br/>      |



 

## <a name="guidelines"></a>Consignes

### <a name="usage"></a>Utilisation

-   **Utilisez le son avec une contrainte pour** vous assurer qu’il existe un avantage global pour l’utilisateur. Concentrez-vous sur les sons qui tiennent les utilisateurs informés, qui seront susceptibles de modifier leur comportement ou de fournir des commentaires utiles. En cas de doute, n’utilisez pas de son.
-   **Sélectionnez le son et ses caractéristiques en fonction de la façon dont il est utilisé.** Pour obtenir une description de chaque modèle d’utilisation, consultez le tableau de la section précédente.
-   **Pour les notifications et les commentaires, n’utilisez pas le son comme seule méthode de communication.** Utilisez plutôt le son comme méthode supplémentaire pour renforcer les signaux visuels ou textuels. Cela garantit que les utilisateurs peuvent voir les informations s’ils ne peuvent pas entendre le son.
-   **Ne lisez pas fréquemment des sons forts ou difficiles.** Cela n’est pas nécessaire et entraîne une expérience utilisateur médiocre. Plus un son est joué, plus le bruit est petit, plus il est discret. Les sons n’ont pas besoin d’être forts ou difficiles pour attirer l’attention.
-   **Ne vous inquiétez pas.** Le signal sonore n’est pas approprié pour les programmes modernes. Les signaux sonores ne peuvent pas avoir des significations spécifiques qui leur sont attribuées et les utilisateurs ne peuvent pas les contrôler.
    -   **Exception :** Les fonctions système critiques peuvent émettre un signal sonore pour alerter les utilisateurs de situations auxquelles elles doivent participer immédiatement, par exemple une alimentation de batterie dangereusement faible.

### <a name="playback"></a>Lecture

-   **Ne pas répéter un son plus de deux fois de suite.**
-   **Pour une séquence consécutive d’événements sonores connexes, jouez un son uniquement sur le premier événement.** Évitez d’utiliser plusieurs sons, car ils peuvent entrer en conflit l’un avec l’autre ou aboutir à une expérience utilisateur déplaisante.

### <a name="sound-selection"></a>Sélection du son

-   **Choisissez des sons agréables.** N’utilisez pas de sons indésirables, tels que le bourdonnement, le plantage et la rupture.
-   **Utilisez des sons courts** (moins d’une seconde).
-   **Utilisez des sons qui sont à peu près le même volume que le son classique Windows.** Les utilisateurs n’ont pas besoin de désactiver le volume au démarrage d’un ordinateur ou d’un programme, en particulier dans des environnements publics tels que des réunions et des présentations. Les fichiers audio Microsoft Windows se trouvent dans le dossier Media dans le dossier Windows.
-   **Ne choisissez pas les sons qui nécessitent une localisation.** Pour ce faire, vous pouvez utiliser des sons qui n’utilisent pas la reconnaissance vocale ou qui ont des significations ou des notations dépendantes de la culture.

### <a name="windows-system-sounds"></a>Sons système Windows

-   **Utilisez les sons système Windows intégrés quand cela est approprié.**
-   **Choisissez d’utiliser des sons système en fonction de leur signification associée, et non simplement du son lui-même.** Les sons système doivent être utilisés de manière cohérente.

### <a name="sound-design"></a>Conception de son

Lors de la création de vos propres sons :

-   **Créez des sons avec les caractéristiques sonores souhaitables.**
-   **Composez des sons avec une fréquence moyenne à des fréquences élevées (de 600 Hz à 2 kHz).** N’utilisez pas de basses fréquences, car elles se déplacent plus loin, sont plus difficiles à localiser et peuvent être alarmes.
-   **Définissez l’amplitude relative des sons normaux sur le niveau du son classique.** Les sons Windows ont été mis à niveau de manière appropriée pour les environnements d’entreprise et de bureau. L’utilisation de différents niveaux pour vos sons oblige les utilisateurs à effectuer des ajustements de volume.
    -   Définissez des sons importants comme étant légèrement plus forts. Ces sons incluent les saisies semi-automatiques des actions, les échecs d’action et les événements système importants.
    -   Définissez les sons les plus fréquents pour qu’ils soient légèrement plus lisses. Il s’agit notamment des FYIs, des sons de personnalisation et des effets sonores.
-   **Choisissez des sons cohérents avec la signification des sons Windows.** Pour créer une version personnalisée d’un son Windows, conservez le même pas et l’intervalle, mais modifiez l’orchestration ou le timbre. N’affectez pas des significations différentes à des sons avec des tonalités et des intervalles similaires à ceux des sons Windows.
-   **Concevez les sons pour que votre programme ressemble à des variations associées sur un thème.** L’expérience d’audit de votre programme doit être coordonnée avec son expérience visuelle.
    -   **Concevoir des transitions de scène et des transitions audio ensemble.** Par exemple, si une scène disparaît graduellement, tout son doit également être progressivement fondu. Ne pas gâcher des transitions visuelles transparents en ayant des transitions sonores brusques.
-   **Les sons doivent être au format de fichier. wav.** Le format PCM (PCM, Pulse Code Modulation) 16 bits 44,1 kHz est recommandé. Si la taille du fichier est importante, utilisez des formats compressés ou mono (mono), mais sachez qu’il existe une perte de qualité facilement discernable qui peut refléter le problème de votre application.

### <a name="mixing"></a>Mixage

-   **N’avez pas de contrôle de volume ou de sourdine dans votre programme.** Au lieu de cela, laissez les utilisateurs contrôler les paramètres de volume relatifs entre les applications avec le mélangeur de volume Windows. Si votre programme a un contrôle de volume, il y aura plusieurs emplacements où les utilisateurs ajusteront leurs paramètres, ce qui peut entraîner une confusion.

    ![capture d’écran du mélangeur de volume Windows ](images/vis-sound-image8.png)

    Le mélangeur de volume Windows permet aux utilisateurs de contrôler le paramètre de volume principal, ainsi que le volume de chaque programme en cours de lecture audio.

<!-- -->

-   **Exception :** Si le but principal de votre programme est la lecture audio ou vidéo ou la création, il peut être utile de disposer d’un contrôle du volume dans le programme. Utilisez un contrôle Slider à cet effet et fournissez des commentaires immédiats lorsque l’utilisateur modifie le volume.

### <a name="windows-integration"></a>Intégration de Windows

-   **Enregistrez les sons de votre programme dans le registre des sons Windows.** Cela permet au mélangeur de volume Windows d’ajouter un curseur pour votre programme.
-   **Inscrivez les événements sonores personnalisés de votre programme.** Cela permet à l’élément du panneau de configuration Windows Sound de les afficher. Créez la clé suivante pour chaque événement sonore personnalisé : HKEY \_ Current \_ User \| AppEvents \| Event labels \| EventName = Event Name.
-   **Ne vous inquiétez pas des sons pour les événements sonores de votre programme.** Au lieu de cela, spécifiez les sons à lire à l’aide des entrées de registre. Cela permet aux utilisateurs de personnaliser les événements sonores via l’élément du panneau de configuration du son.
    -   **Exception :** Vous pouvez choisir de les utiliser pour la personnalisation.
-   **Ne fournissez pas de moyen aux utilisateurs de configurer des sons dans les options de votre programme.** Utilisez plutôt l’élément du panneau de configuration sons Windows à cet effet.
-   **N’assignez pas de sons par défaut aux événements qui se produisent fréquemment.** N’exigez pas des utilisateurs qu’ils configurent leur chemin d’une expérience initiale ennuyeux.

### <a name="directsound-programming-issues"></a>Problèmes de programmation DirectSound

-   Pour les programmes DirectSound qui ont leur propre contrôle de volume, **Définissez le volume de programme sur 100 pour cent par défaut.** Cela optimise la plage dynamique de vos données audio.
-   **Ne verrouillez pas d’autres événements audio en exécutant votre programme en mode exclusif.** Cela peut empêcher les autres programmes de fonctionner correctement. Par exemple, l’utilisation du mode exclusif empêche l’utilisation d’un ordinateur en tant qu’appareil de téléphonie.

## <a name="text"></a>Text

-   N’utilisez pas l’expression carte son. Utilisez une carte son à la place.
-   Utilisez l’appareil pour faire référence de manière générique aux haut-parleurs, aux casques et aux microphones.
-   Utilisez le contrôleur pour faire référence au matériel audio qui contrôle les appareils, tels que les cartes son et les chipsets.
-   Utilisez le modèle de son expression pour décrire une collection de sons pour les événements de programme courants, tels que la connexion ou la réception de nouveaux messages électroniques. Utilisez l’expression thème de bureau pour décrire une collection d’éléments visuels et de sons pour le Bureau de votre ordinateur.
-   Utilisez le terme audio pour faire référence à la reconnaissance vocale, à la musique et aux sons. Utilisez le terme son pour vous référer plus précisément au programme et aux sons Windows décrits dans cet article.

 

