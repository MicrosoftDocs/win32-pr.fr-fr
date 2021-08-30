---
description: cette rubrique fournit une vue d’ensemble conceptuelle de la technologie d’interface utilisateur multilingue (MUI), la prise en charge de la plateforme qu’elle fournit pour l’activation de l’expérience utilisateur multilingue et les avantages qu’elle offre à l’écosystème Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Vue d’ensemble de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6893c6483fff33e251718b243a8a7b02148f1f6d65845eea831930184cfee381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040756"
---
# <a name="overview-of-mui"></a>Vue d’ensemble de MUI

cette rubrique fournit une vue d’ensemble conceptuelle de la technologie d’interface utilisateur multilingue (MUI), la prise en charge de la plateforme qu’elle fournit pour l’activation de l’expérience utilisateur multilingue et les avantages qu’elle offre à l’écosystème Windows.

Sur cette page :

-   [Besoin de l’informatique multilingue](#the-need-for-multilingual-computing)
-   [Rôle de MUI dans l’activation de l’informatique multilingue](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Concepts de base de MUI](#core-concepts-of-mui)
-   [Historique de MUI dans Windows](#history-of-mui-in-windows)
-   [Avantages de la technologie MUI](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>Besoin de l’informatique multilingue

Pour tirer parti des opportunités de croissance présentées par les marchés internationaux, les plateformes et les applications de Microsoft prennent en charge plus de langues, de cultures et de marchés que jamais.

La langue, la culture et les spécificités du marché sont toujours extrêmement pertinentes pour les utilisateurs internationaux, malgré l’amélioration des tendances de globalisation. Le graphique à secteurs suivant montre que les orateurs non anglophones composent toujours 91,5% de la population mondiale.

![graphique à secteurs avec trois segments ; l’une des « enceintes non anglaises 91,5% » est considérablement plus grande que les deux autres.](images/overview-of-mui-fig1.gif)

Dans le monde entier, il existe 193 pays et plus de 6 900 langues connues en cours d’utilisation. En anglais, en dépit de son rôle de langage professionnel, n’est parlé que de 8,5% du remplissage du monde en tant que premier ou deuxième langage. Pour fournir des informations natives à 94% de la population mondiale, ces informations doivent être disponibles dans le 347 (environ 5%) des langues du monde qui ont au moins un million d’orateurs. Cela est particulièrement vrai lorsque les tendances de globalisation ont augmenté les attentes de ces utilisateurs concernant la technologie et leur disponibilité sur leurs marchés.

le besoin de localiser des logiciels dans un plus grand nombre de langues a augmenté au fil des années et Microsoft fournit désormais Windows Vista et d’autres produits dans plus de langues que jamais. cette évolution est particulièrement claire avec Microsoft Windows, car elle vient de la prise en charge de 30 langues avec Windows de 98 à presque 100 avec Windows Vista, comme illustré dans le graphique à barres suivant.

![graphique à barres indiquant que le nombre de langues est bien plus important dans Windows Vista que dans Windows 98 ou Windows XP](images/overview-of-mui-fig2.gif)

*Figure 2 : nombre de langues prises en charge par les versions de Microsoft Windows*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>Rôle de MUI dans l’activation de l’informatique multilingue

Comme nous l’avons vu dans la section précédente, la [globalisation](glossary-for-understanding-mui.md) et la [localisation](glossary-for-understanding-mui.md) des applications sont devenues une nécessité dans un monde plus intégré dans le monde entier. En particulier, à mesure que de plus en plus d’entreprises sont en général, soit en interne, soit via leurs réseaux d’entreprise, la nécessité d’applications multilingues augmente considérablement. Voici donc les obstacles auxquels ces sociétés sont confrontés pour le déploiement global de ces applications.

la prise en charge d’un plus grand nombre de langues pour Windows systèmes d’exploitation, ainsi que d’applications logicielles conçues pour la plateforme Windows, nécessite de nouvelles stratégies qui permettent d’implémenter tous les principaux scénarios avec une surcharge d’ingénierie minimale.

la technologie MUI est destinée aux développeurs et aux éditeurs de logiciels indépendants visant à créer et à prendre en charge des applications multilingues pour la plate-forme Windows. MUI est également très important pour les oem et les entreprises, qui peuvent en tirer parti pour déployer le système d’exploitation Windows et ajouter des applications aux ordinateurs dans différentes langues via un déploiement d’image unique.

## <a name="core-concepts-of-mui"></a>Concepts de base de MUI

L’idée fondamentale de MUI est de [séparer le stockage des ressources localisables du code source](mui-fundamental-concepts-explained.md)de l’application, de façon à pouvoir concevoir une application multilingue comme une combinaison d’un binaire de base indépendant de la langue et d’un ensemble de fichiers de ressources localisés spécifiques à une langue.

Une fois que le code source de l’application est stocké séparément des ressources localisées, il devient facile de [charger dynamiquement les ressources localisées appropriées](mui-fundamental-concepts-explained.md) pour un contexte d’application donné en fonction d’une logique qui prend en compte les paramètres du système, de l’utilisateur et de l’application pour la langue de l’interface utilisateur.

Ces attributs fondamentaux de l’interface MUI facilitent les scénarios d’entreprise tels que :

-   Un modèle de localisation amélioré pour l’interface utilisateur et le contenu de l’aide, grâce à la séparation physique du code source de l’application et des ressources localisables.
-   Traitement des ressources localisables en tant que contenu dynamique et chargement de celles-ci en fonction des paramètres de langue de l’interface utilisateur et des préférences de secours. Cela permet des scénarios tels que :
    -   Passage d’une langue d’interface utilisateur à une autre au moment de l’exécution.
    -   Création d’images de déploiement unique régionales ou mondiales qui couvrent un ensemble de langues pour les OEM et les entreprises.

## <a name="history-of-mui-in-windows"></a>Historique de MUI dans Windows

le niveau de prise en charge disponible pour une expérience utilisateur multilingue au niveau du système d’exploitation Windows et pour le développement d’applications multilingues sur la plateforme Windows a évolué au fil du temps et dans les différentes versions de Windows.

les fonctionnalités prises en charge [avant Windows Vista](evolution-of-mui-support-across-windows-versions.md) étaient assez basiques, avec des images de Windows en une seule langue et une option pour les packs d’interface utilisateur multilingue supplémentaires dans des scénarios spécifiques. Aucune prise en charge de développeur pour les applications multilingues n’était disponible.

[avec Windows vista](evolution-of-mui-support-across-windows-versions.md), Microsoft a fait un investissement significatif dans MUI et Windows Vista est entièrement basé sur une plateforme mui. bien que cela représente une avancée majeure dans Windows stratégie de localisation, car il s’agit d’un activateur clé permettant à Microsoft de fournir des Windows dans un plus grand nombre de langages que jamais auparavant, il est tout d’abord essentiel pour les utilisateurs Windows, les développeurs et les clients. Il offre plusieurs avantages majeurs tels que :

-   Un système d’exploitation indépendant du langage avec prise en charge intégrée de MUI.
-   L’empaquetage, le déploiement et l’installation configurables pour prendre en charge les scénarios multilingues.
-   Déploiement d’une seule image avec plusieurs langues.
-   Modèle de maintenance amélioré dans lequel le code exécutable peut être mis à jour indépendamment des ressources.
-   Prise en charge des développeurs pour la création d’applications multilingues.

le tableau suivant fournit une présentation détaillée de la prise en charge de la plateforme Windows pour MUI :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Assistance</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>versions de Windows prises en charge (prise en charge du système d’exploitation uniquement)</td>
<td><ul>
<li>Windows 2000 Professionnel</li>
<li>famille de serveurs Windows 2000</li>
<li>Windows XP Professionnel</li>
<li>Windows XP Édition Tablet PC</li>
<li>Famille Windows Server 2003.</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>versions de Windows prises en charge (système d’exploitation & prise en charge des applications)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Versions de Windows non prise en charge</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows J'</li>
<li>Windows XP Édition familiale</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Avantages de la technologie MUI

MUI a un impact positif sur plusieurs aspects de l’écosystème Windows :

-   [avantages pour les développeurs](benefits-of-mui-explained.md): de nombreux avantages sont offerts aux développeurs d’applications grâce à la disponibilité de la prise en charge de l’API MUI pour créer des applications multilingues modélisées selon les mêmes principes que la prise en charge multilingue dans le système d’exploitation principal Windows. Les avantages sont les suivants :
    -   La possibilité de fournir une expérience de langue d’affichage conforme à ce que le système d’exploitation lui-même offre.
    -   La possibilité d’étendre facilement la prise en charge linguistique pour une application.
    -   La possibilité de gérer et de traiter facilement l’application.
    -   La possibilité d’activer le déploiement d’une seule image d’applications par les fabricants d’ordinateurs OEM.
-   [Avantages pour les entreprises](benefits-of-mui-explained.md): le principal avantage que MUI offre aux entreprises est la possibilité de déployer, de prendre en charge et de conserver la même image multilingue dans le monde entier avec une seule installation. Une autre victoire importante est la possibilité de prendre en charge des postes de travail multilingues qui offrent une interaction transparente aux utilisateurs avec différentes préférences linguistiques.
-   [Avantages pour les fabricants OEM](benefits-of-mui-explained.md): l’avantage majeur pour les OEM est l’installation d’image unique que MUI active, avec la prise en charge de plusieurs langues, ce qui permet une gestion plus efficace de l’inventaire. Les OEM tirent également parti de la prise en charge MUI pour le développement d’applications, car elles permettent de fournir des applications à valeur ajoutée sur leurs images tout en bénéficiant de l’installation d’une seule image, à condition que ces applications soient compatibles avec l’interface MUI.

 

 




