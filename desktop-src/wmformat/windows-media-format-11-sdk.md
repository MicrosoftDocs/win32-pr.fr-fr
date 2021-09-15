---
title: Windows Kit de développement logiciel (SDK) Media format 11
description: Windows Kit de développement logiciel (SDK) Media format 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Media Format SDK, à propos de
- Windows SDK Media
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), à propos de
- ASF (format de systèmes avancés), à propos de
- Windows Media Format SDK, fonctionnalités
- Windows Media Format SDK, fonctionnalités clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521017"
---
# <a name="windows-media-format-11-sdk"></a>Windows Kit de développement logiciel (SDK) Media format 11

cette documentation décrit le kit de développement logiciel (sdk) de Format Microsoft Windows Media et s’applique aux versions 32 bits et x64 du kit de développement logiciel (sdk).

le kit de développement logiciel (sdk) Windows media Format est un composant du kit de développement logiciel (sdk) Microsoft Windows media. les autres composants incluent le kit de développement logiciel (sdk) Services Windows Media Windows, le kit de développement logiciel (sdk) media encoder, le sdk Windows media Rights Manager, Windows media Gestionnaire de périphériques sdk et Lecteur Windows Media sdk.

le kit de développement logiciel (SDK) Windows media format offre aux développeurs d’applications un accès aux composants du format Windows media. ces composants incluent le conteneur de fichiers ASF (Advanced Systems Format), les codecs vidéo et Windows Media Audio, la fonctionnalité de streaming réseau de base et la gestion des droits numériques. les objets du kit de développement logiciel (SDK) Windows media Format manipulent les composants de Windows média à un niveau bas ; les autres composants du kit de développement logiciel (SDK) Windows Media incluent des objets qui fonctionnent à un niveau supérieur.

l’objectif principal du kit de développement logiciel (SDK) de Format multimédia Windows consiste à permettre aux développeurs de créer des applications qui lisent, écrivent, modifient, chiffrent et fournissent des fichiers ASF (Advanced Systems Format) et des flux réseau. ces fichiers et flux contiennent généralement du contenu audio et vidéo encodé à l’aide des codecs Windows Media Audio et vidéo. Toutefois, ASF peut contenir n’importe quel type de données. Pour plus d’informations sur la structure de conteneurs de format de systèmes avancés, consultez [vue d’ensemble du format ASF](overview-of-the-asf-format.md).

les principales fonctionnalités du kit de développement logiciel (SDK) Windows Media Format sont les suivantes :

-   Prise en charge des codecs les plus performants du secteur. le kit de développement logiciel (SDK) Windows Media Format 11 comprend le codec microsoft Windows Media Video 9 et le codec microsoft Windows Media Audio 9,1. Ces deux codecs fournissent un encodage exceptionnel du contenu multimédia numérique. nouveauté de cette version : le codec de profil avancé Windows Media Video 9, qui fournit des optimisations pour la diffusion vidéo. ce kit de développement logiciel (SDK) comprend également le codec d’écran Microsoft Windows Media Video 9 permettant de compresser l’activité de l’écran de l’ordinateur pendant les sessions des applications de l’utilisateur, ainsi que le codec vocal Windows Media Audio 9,1, qui encode les données audio de faible complexité, telles que la parole et s’adapte intelligemment à un son plus complexe, par exemple la musique
-   Prise en charge de l’écriture de fichiers ASF. Les fichiers sont créés en fonction de profils personnalisables, ce qui facilite la configuration et la normalisation des fichiers. Ce kit de développement logiciel (SDK) peut être utilisé pour écrire des fichiers d’une capacité supérieure à 2 gigaoctets, ce qui permet d’obtenir des fichiers continus plus longs et de qualité.
-   Prise en charge de la lecture des fichiers ASF. Ce kit de développement logiciel (SDK) prend en charge la lecture des fichiers ASF locaux, ainsi que la lecture des données ASF diffusées en continu sur un réseau. La prise en charge est également fournie pour de nombreuses fonctionnalités de lecture avancées, telles que la prise en charge native des fichiers de débit binaire multiple (MBR), qui contiennent plusieurs flux avec le même contenu encodé à des vitesses de transmission différentes. Le lecteur sélectionne automatiquement le flux MBR à utiliser, en fonction de la bande passante disponible au moment de la lecture.
-   Prise en charge de la diffusion de flux ASF sur un réseau. ce kit de développement logiciel (SDK) prend en charge la diffusion de données ASF via HTTP vers des ordinateurs distants sur un réseau, ainsi que la transmission de données directement à un serveur multimédia Windows distant.
-   Prise en charge de la modification des métadonnées dans les fichiers ASF. Les informations relatives à un fichier et son contenu sont manipulées facilement avec ce kit de développement logiciel (SDK). Les développeurs peuvent utiliser le système robuste d’attributs de métadonnées inclus dans le kit de développement logiciel (SDK), ou créer des attributs personnalisés en fonction de leurs besoins.
-   Prise en charge des applications de modification de contenu. Ce kit de développement logiciel (SDK) permet aux applications de rechercher des points dans un fichier par heure de présentation et par image vidéo. en outre, les fichiers créés à l’aide du kit de développement logiciel (SDK) Windows Media Format peuvent gérer les horodateurs dans les formats utilisés dans la production de films et de télévision.
-   Prise en charge de la lecture et de la modification des métadonnées dans les fichiers MP3. Ce kit de développement logiciel (SDK) fournit une prise en charge intégrée pour la lecture des fichiers MP3 avec les mêmes méthodes que celles utilisées pour lire les fichiers ASF. les Applications générées à l’aide du kit de développement logiciel (SDK) Windows Media Format peuvent également modifier les attributs de métadonnées dans les fichiers MP3 grâce à la prise en charge intégrée des balises ID3 les plus courantes utilisées par les créateurs de contenu.
-   Prise en charge de la protection Rights Management numérique. Ce kit de développement logiciel (SDK) fournit des méthodes pour lire et écrire des fichiers ASF et des flux réseau protégés par des Rights Management numériques afin d’empêcher la lecture ou la copie non autorisée du contenu.

pour télécharger le kit de développement logiciel (SDK) Windows media Format, consultez la page de [téléchargements Windows media](https://msdn.microsoft.com/windows/desktop/aa904949) sur le site Web de Microsoft.

ce document décrit comment vous pouvez développer des applications multimédias numériques à l’aide du kit de développement logiciel (SDK) de Format multimédia Windows. Elle est divisée en sections suivantes.

> [!Note]  
> bien que ce document contienne des informations sur la dernière version du kit de développement logiciel (sdk) Windows Media Format, la plupart des fonctionnalités qu’il décrit sont prises en charge par les versions antérieures du kit de développement logiciel (sdk). les pages de référence pour les méthodes, les fonctions, les structures et les énumérations du kit de développement logiciel (SDK) Windows Media Format incluent les spécifications de version.

 



| Section                                                                                                          | Description                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [à propos du kit de développement logiciel (SDK) Windows Media Format](about-the-windows-media-format-sdk.md)                                     | Fournit une vue d’ensemble et des informations générales que vous devez connaître avant de tenter de créer des applications.                                                                                  |
| [Guide de programmation](programming-guide.md)                                                                       | Fournit des instructions détaillées pour effectuer diverses tâches, telles que la lecture, l’écriture et l’indexation de fichiers, la protection des fichiers avec des Rights Management numériques, la diffusion en continu de données ASF sur un réseau, etc. |
| [Guide de référence de programmation](programming-reference.md)                                                               | fournit des informations de référence pour les interfaces, les méthodes, les fonctions, les structures, les types énumération et les constantes relatives à Windows Format multimédia.                                                     |
| [Windows Interfaces de codec audio et vidéo multimédia](windows-media-audio-and-video-codec-interfaces--deprecated.md) | fournit des instructions pour Windows Media Audio l’utilisation directe des DMOs et Video codec digital Media objects ().                                                                                           |
| [*Glossaire*](wmformat-glossary.md)                                                                              | définit les termes utilisés dans la documentation du kit de développement logiciel (SDK) Windows Media Format.                                                                                                                                    |



 

 

 




