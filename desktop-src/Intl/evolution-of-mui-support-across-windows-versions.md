---
description: évolution de la prise en charge MUI sur les Versions Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: évolution de la prise en charge MUI sur les Versions Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e08ff181cf34daa95710d5bf57a294703a88ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240323"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>évolution de la prise en charge MUI sur les Versions Windows

-   [avant Windows Vista](#before-windows-vista)
-   [Windows Vista et versions ultérieures](#windows-vista-and-beyond)
    -   [Un système d’exploitation indépendant de la langue/MUI](#a-language-neutralmui-operating-system)
    -   [Les scénarios de déploiement sont entièrement basés sur MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Déploiement d’une seule image](#single-image-deployment)
    -   [Amélioration du modèle de service](#improved-servicing-model)
    -   [Infrastructure MUI](#mui-infrastructure)
    -   [Gestion des langues](#language-management)
    -   [Gestion des ressources](#resource-handling)

## <a name="before-windows-vista"></a>avant Windows Vista

avant la version Windows Vista, Windows fournies avec des images de langue unique, ce qui signifiait que chaque version localisée de Windows contenait une seule langue pour son interface utilisateur. MUI était un module complémentaire de la version anglaise du système d’exploitation, et les packs de interface utilisateur multilingue pouvaient uniquement être ajoutés à certaines versions anglaises de Windows. en cas d’installation sur la version anglaise de Windows, MUI permettait de modifier la langue de l’interface utilisateur du système d’exploitation en fonction des préférences des utilisateurs individuels dans l’une des langues prises en charge.

Le modèle MUI Pack n’a pas pu exposer la prise en charge MUI pour les applications. Bien que les développeurs puissent créer des applications multilingues, ils devaient créer leurs propres mécanismes pour le faire.

## <a name="windows-vista-and-beyond"></a>Windows Vista et versions ultérieures

avec Windows Vista, Microsoft a fait un investissement significatif dans MUI. Windows Vista est entièrement basé sur une plateforme MUI. bien que cela représente une avancée majeure dans Windows stratégie de localisation, car il s’agit d’un activateur clé permettant à Microsoft de fournir des Windows dans un plus grand nombre de langues que jamais précédemment, il est tout d’abord essentiel pour les utilisateurs Windows et les clients.

### <a name="a-language-neutralmui-operating-system"></a>Un système d’exploitation indépendant de la langue/MUI

la grande majorité des binaires de Windows Vista sont compatibles avec MUI et leurs données localisables sont stockées séparément du code. Cela offre une certaine flexibilité, car différentes données de langage peuvent être ajoutées à tout moment.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Les scénarios de déploiement sont entièrement basés sur MUI

la conception de l’empaquetage et de l’installation de Windows Vista est basée sur MUI et toutes les données localisables sont empaquetées dans des packs spécifiques à la langue, et chaque module linguistique peut être déployé dans différents scénarios. par exemple, bien que les dvd commercialisés pour Windows Vista contiennent des versions en une seule langue, les utilisateurs de l’édition Ultimate peuvent télécharger des modules linguistiques MUI supplémentaires et modifier la langue de l’interface utilisateur à partir des **Options régionales et linguistiques** du panneau de configuration. les licences Enterprise edition permettent d’accéder à toutes les langues et de les déployer.

### <a name="single-image-deployment"></a>Déploiement d’une seule image

Enterprise clients et les fabricants d’ordinateurs oem peuvent désormais réduire le nombre d’images dont ils ont besoin pour déployer des Windows et des applications sur des ordinateurs situés sur des paramètres régionaux différents via un déploiement d’image unique.

avec MUI sur Windows Vista, une image contenant plusieurs langues peut être déployée sur n’importe quel utilisateur de langage, et les utilisateurs peuvent déterminer leurs propres langues préférées (dans la stratégie) au cours de l’installation ou de la première utilisation de l’ordinateur. En particulier, les fabricants d’ordinateurs OEM peuvent placer de nombreux langages d’interface utilisateur sur leurs nouveaux ordinateurs pour permettre aux utilisateurs d’en sélectionner un à partir du centre d’accueil. Ainsi, à partir d’une image avec plusieurs modules linguistiques, le programme d’installation affiche une liste des langues disponibles et permet aux utilisateurs de choisir l’un d’entre eux. Tous les paramètres internationaux sont ensuite définis pour correspondre à la langue ou aux paramètres régionaux sélectionnés.

### <a name="improved-servicing-model"></a>Amélioration du modèle de service

Le même package QFE ou correctif de sécurité peut désormais être installé sur tous les systèmes de langue. Cela est essentiel, car il permet une plus grande rapidité des correctifs de sécurité et permet à tous les utilisateurs internationaux de tirer parti de la même durée de disponibilité de tous les correctifs de sécurité.

### <a name="mui-infrastructure"></a>Infrastructure MUI

à compter de Windows Vista, les api mui sont disponibles pour permettre aux développeurs de tirer parti des mécanismes MUI pour leurs propres applications, sans avoir à créer une logique personnalisée pour la gestion des ressources et la gestion des langues.

### <a name="language-management"></a>Gestion des langues

Les API MUI de base qui fournissent des fonctionnalités de gestion de la langue de l’interface utilisateur sont disponibles dans le cadre de l’infrastructure MUI. Pour faciliter la gestion des différents paramètres de langue de l’interface utilisateur au niveau du système, de l’utilisateur et de l’application, MUI les combine en interne dans une liste hiérarchisée unique. MUI implémente ensuite un mécanisme de secours basé sur cette liste hiérarchisée, ce qui permet d’utiliser des solutions de localisation partielles tout en fournissant aux utilisateurs une expérience de langue d’interface utilisateur appropriée, si elle n’est pas préférée.

par exemple, un système exécutant la version espagnole de Windows Vista avec un pack d’interface linguistique Catalan (LIP) installé sur le système d’exploitation de base peut prendre en charge le comportement suivant : le système essaiera d’abord d’afficher ses ressources dans le catalan et, si ces ressources ne sont pas disponibles en catalan, fournissez à l’utilisateur des ressources espagnoles à la place.

### <a name="resource-handling"></a>Gestion des ressources

avec l’infrastructure mui améliorée qui est disponible à partir de Windows Vista, la plupart des technologies de ressources courantes sont compatibles avec l’interface mui. le tableau suivant fournit des informations supplémentaires sur la prise en charge de la gestion des ressources disponible dans Windows Vista.




| Category | Support | 
|----------|---------|
| Types de ressources pris en charge | <ul><li>Ressource Win32/non managée : .DLL/.EXE/. OCX</li><li>Inscriptions liées à l’interpréteur de commandes</li><li>Ressources liées à la gestion : journal des événements, fichiers de composant logiciel enfichable/MSC</li><li>WMI : MOF/MFL</li><li>Stratégie de groupe : ADMX/ADML</li><li>Resources.dll géré</li></ul> | 
| Outils de développement | <ul><li>pour Win32 : RC.exe, MUIRCT.exe et Visual Studio 2005 et versions ultérieures</li></ul> | 
| Prise en charge limitée des types de ressources | <ul><li>fichiers d’aide *. chm</li></ul> | 




 

 

 



