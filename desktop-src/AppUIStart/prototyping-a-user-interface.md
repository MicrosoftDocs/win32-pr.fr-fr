---
title: Prototypage d’une interface utilisateur
description: Cette rubrique décrit comment le prototypage d’une interface utilisateur peut aider à réduire les défauts de conception et garantir une expérience utilisateur réussie.
ms.assetid: 16e3fabb-9cd1-4517-8f19-b1d80c956ee0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce42ad4240c3a06716f0db851e98b31e713b1ce0e23d1d485bc3e154375d9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507433"
---
# <a name="prototyping-a-user-interface"></a>Prototypage d’une interface utilisateur

Cette rubrique décrit comment le prototypage d’une interface utilisateur peut aider à réduire les défauts de conception et garantir une expérience utilisateur réussie.

## <a name="introduction"></a>Introduction

Parfois, au fur et à mesure qu’un projet progresse, les petites hypothèses et les bonnes décisions s’accumulent, transformant les heures de travail en une expérience utilisateur miteux. Les équipes intelligentes éliminent leurs erreurs avant qu’elles ne soient expédiées à l’aide d’une technique appelée prototypage d’interface utilisateur. Combinés aux études de convivialité, les prototypes conservent les équipes dans le sens approprié.

## <a name="why-prototype"></a>Pourquoi procéder à un prototype ?

Le prototypage est un moyen d’explorer les idées avant de les investir. Tous les craftspeople et ingénieurs expérimentés créent des prototypes de leur travail avant de générer quoi que ce soit : les architectes créent des modèles à partir de papier ou de carton, ou avec des outils de réalité virtuelle. Les ingénieurs Aeronautic utilisent des tunnels à vent. Les générateurs de pont créent des modèles de stress. Les concepteurs de logiciels et de sites Web créent des maquettes de la façon dont les utilisateurs interagissent avec leurs conceptions.

La meilleure raison de procéder au prototype est de gagner du temps et des ressources. La valeur d’un prototype est qu’il s’agit d’une façade, comme un ensemble Hollywood, où seule la partie avant de la construction est construite. Par rapport au produit réel, les prototypes sont faciles à créer. Ainsi, pour un investissement minimal, les problèmes d’utilisation et de conception peuvent être détectés et l’interface utilisateur est ajustée avant l’investissement substantiel dans la conception et les technologies finales.

En cas d’examen des besoins d’un projet particulier, il est possible de trouver des raisons de créer un prototype autre que l’enregistrement de l’argent. L’objectif est-il d’explorer un nouveau modèle d’interface ? Apporter des modifications à une partie de la conception existante ? Vous recherchez une nouvelle technologie ? Avant de commencer, il est important de comprendre pourquoi vous créez ce que vous créez. En commençant par des objectifs clairs, vous contribuez à l’effort direct et efficace. Les raisons justifiant la création de prototypes se répartissent en trois catégories :

-   Preuve de concept.

    Dans certaines équipes, il y a des désaccords à propos de l’orientation future d’un projet. Un prototype peut être utilisé pour prouver qu’une idée ou une nouvelle approche a une valeur ou une valeur. Un prototype peut aider à illustrer le fonctionnement d’une idée, exprimer ses qualités de manière visuelle et interactive, et/ou motiver les membres de l’équipe à réfléchir au problème d’une autre perspective.

-   Conception de l’exploration.

    Si vous concevez des logiciels interactifs, la seule façon d’explorer l’utilisation consiste à créer une maquette et à interagir avec elle. Parfois, le simulacre est lié à une étude d’utilisabilité, où des parties du prototype peuvent être évaluées de façon structurée. Parfois, il s’agit simplement d’un moyen d’exprimer clairement à un développeur le fonctionnement ou l’apparence d’un événement. Dans de nombreux cas, un concepteur peut simplement être expérimentant, dans le but d’avoir une idée de l’approche qui peut fonctionner. Toute personne de l’équipe peut utiliser des prototypes pour explorer les problèmes de conception, bien que les concepteurs soient généralement les plus compétents. Les explorations de conception doivent être dirigées vers la tentative de résolution de problèmes spécifiques qui sont reconnus dans le produit.

-   Exploration technique.

    Les développeurs qui étudient les approches d’implémentation d’un problème essaient souvent d’essayer différentes techniques de codage pour voir s’ils fonctionnent correctement. L’utilisation de COM+, Dynamic HTML (DHTML), Microsoft Win32 ou des approches de codage spécifiques au sein de chaque technologie présente des compromis différents. Parfois, un prototype représente une exploration de la technologie adaptée à la prise en charge d’une certaine fonctionnalité de l’interface utilisateur.

Parfois, des prototypes sont créés pour une combinaison de ces raisons. Si une équipe planifie suffisamment bien, elle peut allouer du temps à un développeur et à un concepteur ou chef de projet de travailler ensemble sur un prototype. Dans ce cas, il est extrêmement important de définir clairement les objectifs et les contributions que chaque membre de l’équipe est censé effectuer. Tout le monde doit être clair sur ce que sont les objectifs, sur ce qui est en jeu et sur le résultat potentiel.

## <a name="who-is-involved"></a>Qui Est impliqué ?

Le prototypage peut être effectué de manière informelle par n’importe qui, indépendamment de son arrière-plan ou de son rôle dans le projet. Il est facile de créer un prototype simple mais efficace en utilisant une image bitmap d’Adobe Photoshop, en la plaçant dans l’outil de création et de gestion de sites Web Microsoft FrontPage, et en ajoutant des boutons ou des liens actifs. Ces prototypes légers ne vont jusqu’à présent et peuvent devenir peu maniables pour les interactions complexes.

Pour les prototypes plus formels par des équipes de plus grande taille, un développeur ou un responsable de projet collaborera souvent avec un concepteur et un ingénieur d’utilisation. Ensemble, ils génèrent des idées, créent un prototype qui représente les meilleures idées, puis entrent dans le laboratoire pour déterminer l’efficacité de la résolution des problèmes des utilisateurs. Les développeurs peuvent être impliqués s’ils peuvent se faire passer du temps ou si leur expertise technique est nécessaire. Souvent, le concepteur ou le responsable de projet effectuera la plupart des scripts ou du codage pour générer le prototype.

## <a name="when-should-a-prototype-be-built"></a>Quand un prototype doit-il être généré ?

En fonction de l’étendue du prototype et du niveau de détail requis, les prototypes peuvent être générés à tout moment pendant le projet. La plupart du temps, ils sont créés tôt dans le projet, pendant la phase de planification et de spécification, avant que les développeurs écrivent du code de production. C’est à ce moment-là que le besoin d’exploration est le plus grand et que le temps d’investissement nécessaire est le plus viable. Si les développeurs, plutôt que les responsables de programme ou les concepteurs, sont des prototypes, le temps de planification devient encore plus important en raison de la nécessité de s’assurer que le travail investi dans le prototype est comptabilisé dans le calendrier de développement. La planification d’une version de l’interface utilisateur doit inclure un certain niveau de prototypage.

Dans un projet, les prototypes plus petits peuvent aider à résoudre les problèmes techniques et de conception difficiles. Une maquette HTML rapide de la façon dont une boîte de dialogue ou une page Web doit se comporter peut aider à répondre à la question d’un développeur ou à d’autres coéquipiers comme l’expérience souhaitée. dans certains cas, un responsable de programme ou un concepteur puissant peut implémenter le comportement dans le logiciel de développement JScript Microsoft et se rapprocher d’une grande partie de la logique de programmation que les développeurs doivent réfléchir.

Le temps nécessaire à la création d’un prototype peut varier considérablement, en fonction de l’étendue et de la précision de ce à quoi doit ressembler le résultat final. Un prototype informel peut signifier quelques heures de travail par une personne ; un effort plus organisé peut impliquer des semaines d’effort par une équipe entière.

## <a name="where-should-the-focus-be"></a>Où se trouve le focus ?

Dans un prototype, générez uniquement la plus grande partie de la conception en fonction des besoins. Il est possible d’avoir des boutons qui ne fonctionnent pas ou du texte qui n’est jamais mis à jour. Tant que les interactions requises peuvent être rencontrées, il est parfait d’utiliser la fumée et les miroirs pour le reste. Voici quelques raisons pour lesquelles les efforts doivent être ciblés avec soin :

-   Coût de la création du prototype.

    Le coût nécessaire à la création du prototype doit être réduit. Le défi de la création de prototypes consiste à reconnaître les investissements minimaux nécessaires pour répondre efficacement aux questions sur la conception. C’est là que les études de convivialité sont critiques, car elles identifient clairement les parties de l’interface utilisateur qui nécessitent le plus de travail. Même sans les études de convivialité, définissez clairement les problèmes d’utilisateur qui sont résolus, ou les tâches qui sont améliorées, avec la conception dans le prototype.

-   Durée de vie limitée.
-   Les prototypes doivent avoir des durées de vie clairement définies. L’objectif final est-il une présentation au cours d’une réunion d’équipe ? Une réunion de révision de la direction ? Une revue des spécifications ? Une étude d’utilisabilité ? Vous identifiez que la conception résout un problème de l’utilisateur ? Une fois que les besoins de ces objectifs spécifiques sont atteints, le prototype doit être mis de côté. L’esprit de base est que le code ou les bitmaps générés dans un prototype sont conservés. Il peut y avoir des exceptions où le code ou les éléments visuels se trouvent dans le produit, mais l’attente doit être que cela ne sera pas le cas.
-   Risque de saturation de l’équipe.

    L’illustration de prototypes pour les développeurs et les coéquipiers peut être délicate. Un prototype trop complexe ou élaboré, des visuels et des animations exceptionnels, peuvent surcharger les gens. Toujours avoir un sens pour atteindre et combien de temps le prototype doit être pris au sérieux.

## <a name="what-is-the-scope"></a>Qu’est-ce que l’étendue ?

Au fur et à mesure de la détermination de l’effort de prototypage, tenez compte des points suivants :

-   Besoins du client.

    En commençant par une compréhension des problèmes clés ou des besoins des utilisateurs (peut-être un spécialiste de l’utilisation), vous savez quelles parties de la conception de l’interface utilisateur justifient le plus d’exploration.

-   Tâches d’étude de la convivialité.

    Si vous créez le prototype pour une étude d’utilisabilité, discutez avec l’ingénieur d’utilisation des tâches spécifiques qui feront partie de l’étude et concevez ces éléments.

-   Entrée de l’équipe.

    Communiquez avec les principaux développeurs de l’équipe à mesure que les idées du prototype sont réunies. Vous pouvez obtenir un sens de base pour ce qui est raisonnable, ce qui est possible et ce qui se passe en considération pour la prochaine version. Dans certains cas, il peut être judicieux d’aller au-delà de ce qu’il dit est possible pour un aspect de la conception s’il s’agit d’un point clé et que l’équipe doit être contestée. Toutefois, n’effectuez pas cette opération avec tous les aspects de votre prototype, car il y a une ligne fine entre l’émission des limites et la saturation de votre équipe. Si vous le souhaitez, vous pouvez inspirer l’équipe en l’expliquant comme une vision de plusieurs versions, puis pour y accéder. Toutefois, si l’exigence est de définir des modifications spécifiques pour la prochaine version, concentrez-vous sur ces modifications. Veillez à appeler les modifications spécifiques d’une manière modulaire et à montrer aux développeurs comment créer les conceptions.

-   Largeur et profondeur.

    Pour les prototypes plus importants, il y a une prise en compte supplémentaire de la largeur par rapport à la profondeur. Chaque fonctionnalité de la conception ne doit-elle pas fonctionner un peu, ou doit-elle être choisie pour effectuer un prototype avec presque tous ses éléments et options ? Essayez de ne pas faire les deux, car le résultat peut être un prototype de grande taille et difficile à modifier et difficile à lever.

## <a name="flexible-prototypes"></a>Prototypes flexibles

Une façon de se concentrer sur les ressources de prototypage consiste à se concentrer sur la conception intelligente. Il est possible de créer des prototypes plus efficaces en autorisant un morceau de code de prototype à exercer de nombreuses idées différentes. Au lieu d’avoir cinq prototypes différents, envisagez de créer un prototype qui a les options permettant de changer les différents attributs du prototype.

La barre d’outils doit-elle être située à gauche ou en haut ? Dois-je afficher 10 éléments sur la page d’hébergement ou 20 ? Un bon prototype dispose d’un certain type de panneau d’options intégré qui vous permet de modifier les paramètres de l’apparence ou du fonctionnement du prototype. Gardez ces panneaux d’options masqués dans le prototype : essayez d’éviter qu’un participant à la convivialité les trouve accidentellement pendant un test.

Le défi consiste à garder le prototype simple, mais toujours utile qu’il puisse être présenté à un coéquipier, des options différentes peuvent être démontrées et des commentaires peuvent être obtenus.

## <a name="beta-vs-prototype"></a>Comparaison entre la version bêta et le prototype

Les versions bêta ne sont pas qualifiées de prototypes, car il s’agit d’un effort d’ingénierie complet. Si une erreur critique est détectée dans une fonctionnalité d’une version bêta, il est peu probable qu’elle soit supprimée, même si elle peut être dans le meilleur intérêt du produit. Les développeurs, les testeurs et les concepteurs ont déjà investi beaucoup de temps et la pression sur les mauvaises décisions est très élevée. Les versions bêta vous aident certainement à trouver des bogues et des défauts, mais elles sont rarement utiles pour effectuer des études contrôlées de la valeur des directions de conception spécifiques.

## <a name="tools-and-technologies"></a>Outils et technologies

Il existe plusieurs outils et technologies qui peuvent être utilisés pour créer des prototypes, chacun ayant ses avantages et ses inconvénients. Tenez compte du type de travail de conception qui fait l’objet d’un prototype et des objectifs de l’effort de prototypage avant de décider de l’outil ou de la technologie qui convient le mieux.

-   Microsoft Visual Basic ou C#.

    il s’agit de la technologie la plus rapide pour créer des prototypes d’interface utilisateur de style Windows. l’objet de navigateur Web facilite l’intégration de HTMLUI à des composants de style Windows standard. bien qu’il soit vrai qu’un développeur expérimenté avec Microsoft Visual Studio pourrait être en mesure de générer l’interface utilisateur plus rapidement en C/C++, cela crée la tentation de réutiliser le code du prototype d’interface utilisateur dans le code de production. Il est nécessaire de reconnaître que les objectifs d’un prototype d’interface utilisateur rapide et sale sont très divergents de l’ingénierie de haute qualité. Assurez-vous qu’il s’agit d’un type de code en cours d’écriture et que l’équipe ou le responsable comprend les éléments qui seront ignorés.

-   Microsoft Expression Blend + SketchFlow.

    SketchFlow est un outil visuel permettant de concevoir, de créer des prototypes et de créer des interfaces utilisateur sophistiquées pour les applications de bureau et web de Windows Presentation Foundation (WPF) et Microsoft Silverlight. Les applications sont générées en dessinant des formes, en dessinant des contrôles tels que des boutons et des zones de liste, en faisant en sorte que les parties d’une application répondent aux clics de souris et à d’autres entrées utilisateur, et tout en apportant un style à l’apparence unique.

-   Adobe Director ou Adobe Flash.

    Director est un outil de prototypage d’interface utilisateur populaire parmi les concepteurs. Elle est particulièrement utile pour les conceptions d’interface utilisateur multimédia ou non standard, ou pour les prototypes qui nécessitent une animation importante. C’est une grande flexibilité qui complique l’interface utilisateur de type interface utilisateur par rapport à Visual Basic. toutefois, un utilisateur compétent peut générer Windows ou une interface utilisateur Web sans difficulté.

-   HTML.

    FrontPage et d’autres éditeurs HTML permettent de créer rapidement des prototypes simples. Pour exprimer une idée, il est souvent possible de créer des bitmaps qui illustrent une séquence d’interaction utilisateur et de les placer dans FrontPage. Ces images peuvent être utilisées pour simuler l’interaction avec la conception. JScript et DHTML prennent des mesures à un autre niveau, en permettant une logique et une interaction très sophistiquées. Si vous utilisez du code HTML pour prototyper un site Web, l’avertissement qui vient d’être décrit pour C/C++ s’applique ici également, ne rentre pas dans l’interruption du code de prototype rapide confus avec l’ingénierie de qualité de production.

 

 




