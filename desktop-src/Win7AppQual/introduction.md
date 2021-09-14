---
description: Introduction (Windows 7 et Windows Server 2008 R2 livre de recettes de qualité des applications)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introduction (Windows 7 et Windows Server 2008 R2 livre de recettes de qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4125c2bd122d239c155f089f06bef2f455ee121b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221881"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introduction (Windows 7 et Windows Server 2008 R2 livre de recettes de qualité des applications)

dans le monde entier, de nombreuses entreprises adoptent Windows 7 en raison de ses fonctionnalités et capacités d’entreprise. Les services informatiques changent également la manière dont ils approchent leurs besoins en matière de plateforme à long terme pour prendre en charge un bureau moderne. le système d’exploitation Windows 7 permet de réduire le coût total de possession en aidant les utilisateurs à rester productifs partout, à améliorer la sécurité et le contrôle, et à simplifier la gestion des postes de travail au sein de l’organisation. Windows 7 inclut également un navigateur moderne basé sur des normes, Windows Internet Explorer 8, qui offre une sécurité améliorée et des fonctions de navigation améliorées. Ces deux plateformes augmentent l’efficacité informatique et améliorent l’agilité et la sécurité de l’organisation.

Toutefois, la migration vers un nouveau système d’exploitation crée des défis uniques, principalement avec la nécessité de prendre en charge des applications Web héritées. les entreprises peuvent avoir des applications conçues pour des versions antérieures de Windows internet explorer, comme Windows internet explorer 7 ou Microsoft internet explorer 6. Ces applications Web peuvent rencontrer des problèmes de compatibilité avec Internet Explorer 8. en outre, Internet explorer 6 n’est pas exécuté en mode natif sur Windows 7 et Windows ne prend pas en charge l’exécution simultanée de deux versions d’Internet explorer. Pour plus d’informations, consultez l’article de la base de connaissances Microsoft, «[exécution de plusieurs versions d’Internet Explorer sur un seul système d’exploitation n’est pas pris en charge](https://support.microsoft.com/kb/2020599)».

De nombreuses entreprises utilisent encore des applications Web basées sur Internet Explorer 6 qui ont été créées et personnalisées au cours des dix dernières années. les entreprises qui envisagent de déployer Windows 7 doivent avoir une stratégie complète et un plan d’exécution en place pour migrer les applications web héritées vers Internet Explorer 8. Ce document fournit une vue d’ensemble détaillée des problèmes de compatibilité d’Internet Explorer 8, explique comment migrer des applications Web et présente les outils et processus associés.

La version d’Internet Explorer 8 est axée sur trois thèmes principaux :

-   Offrez une interopérabilité réelle avec d’autres navigateurs et une compatibilité pour les sites Web existants.
-   Rendez le développement Web plus rapide et plus facile grâce aux outils de développement intégrés.
-   Activez les expériences qui s’étendent au-delà de la page, grâce aux nouvelles fonctionnalités de navigateur qui connectent les utilisateurs aux services Web novateurs.

En plus des avancées significatives en matière de prise en charge des normes, Internet Explorer 8 contient des investissements de plateforme supplémentaires pour les développeurs. Internet Explorer 8 améliore les performances dans de nombreux sous-systèmes Internet Explorer, tels que l’analyseur HTML, le traitement des règles de feuille de style en cascade (CSS), la manipulation d’arborescence de balises, l’analyseur JavaScript, le runtime de garbage collector et la gestion de la mémoire. Les investissements supplémentaires pour les développeurs sont les suivants :

-   CSS 2,1 : vous pouvez écrire vos pages une seule fois et les rendre plus faciles à afficher correctement dans différents navigateurs, car Internet Explorer 8 prend entièrement en charge la spécification CSS 2,1.
-   Améliorations apportées à Document Object Model (DOM) et HTML 4,01 : Internet Explorer 8 offre des améliorations supplémentaires au format HTML 4,01 et une conformité CSS 2,1 complète. Internet Explorer 8 résout également de nombreuses incohérences entre les navigateurs. Par exemple, l’implémentation de l’attribut obtenir/Set/Remove est désormais interopérable avec d’autres navigateurs, et les performances sont améliorées dans les modèles de conception asynchrones JavaScript et XML (AJAX).
-   normes émergentes : Internet Explorer 8 intègre les normes futures, telles que w3c HTML5 Draft DOM Stockage standard, l’API des sélecteurs du groupe de travail des Applications Web et la syntaxe approuvée par ECMAScript 3,1.
-   Nouvelles fonctionnalités de navigation pour les applications AJAX : vous pouvez mettre à jour la pile de navigation avant et arrière du navigateur et la barre d’adresses à partir d’une application AJAX pour que ces fonctionnalités de navigateur fonctionnent correctement dans votre application.
-   Acid2 : Internet Explorer 8 restitue correctement le test du navigateur Acid2.
-   Compatibilité : Internet Explorer 8 comprend un moteur de disposition plus compatible avec les normes qui vous permet de créer un site basé sur des normes pour plusieurs navigateurs. Pour migrer plus facilement vos sites vers le nouveau moteur de disposition conforme aux normes, Internet Explorer 8 vous permet d’utiliser le moteur de disposition d’Internet Explorer 7 en insérant un simple **méta** -élément dans votre code ou en ajoutant un seul en-tête http sur vos serveurs.
-   Outils de développement : Outils de développement dans Internet Explorer (auquel vous accédez en appuyant sur la touche F12) vous permet de déboguer rapidement du code HTML, CSS et JavaScript dans un environnement visuel. Ces outils sont inclus directement dans Internet Explorer 8 avec des fonctionnalités étendues, notamment l’option Ann pour choisir l’application à utiliser lorsque vous affichez la source d’une page Web. Vous pouvez rapidement identifier et résoudre les problèmes en raison de l’analyse approfondie que l’outil fournit dans le DOM.
-   Pour plus d’informations sur les nouvelles fonctionnalités améliorées d’Internet Explorer 8, consultez [Nouveautés d’Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) dans MSDN Library.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



