---
title: SDK Windows Media format 11
description: SDK Windows Media format 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Media Format SDK, à propos de
- SDK Windows Media
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), à propos de
- ASF (format de systèmes avancés), à propos de
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- Windows Media Format SDK, fonctionnalités clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463862"
---
# <a name="windows-media-format-11-sdk"></a>SDK Windows Media format 11

Cette documentation décrit le kit de développement logiciel (SDK) Microsoft Windows Media format et s’applique aux versions 32 bits et x64 du kit de développement logiciel (SDK).

Le kit de développement logiciel (SDK) Windows Media format est un composant du kit de développement logiciel (SDK) Microsoft Windows Media. Les autres composants incluent le kit de développement logiciel (SDK) Windows Media Services, le SDK Windows Media Encoder, le kit de développement logiciel Windows Media Rights Manager, le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques et le Windows Media Player

Le kit de développement logiciel (SDK) du format Windows Media offre aux développeurs d’applications un accès aux composants du format Windows Media. Ces composants incluent le conteneur de fichiers ASF (Advanced Systems Format), les codecs vidéo et Windows Media Audio, la fonctionnalité de streaming réseau de base et la gestion des droits numériques. Les objets du kit de développement logiciel (SDK) de format Windows Media manipulent les composants de Windows Media à un niveau bas ; les autres composants du kit de développement logiciel (SDK) Windows Media incluent des objets qui fonctionnent à un niveau supérieur.

L’objectif principal du kit de développement logiciel (SDK) du format Windows Media est de permettre aux développeurs de créer des applications qui lisent, écrivent, modifient, chiffrent et fournissent des fichiers ASF (Advanced Systems Format) et des flux réseau. Ces fichiers et flux contiennent généralement du contenu audio et vidéo encodé à l’aide des codecs Windows Media Audio et vidéo. Toutefois, ASF peut contenir n’importe quel type de données. Pour plus d’informations sur la structure de conteneurs de format de systèmes avancés, consultez [vue d’ensemble du format ASF](overview-of-the-asf-format.md).

Les principales fonctionnalités du kit de développement logiciel (SDK) Windows Media format sont les suivantes :

-   Prise en charge des codecs les plus performants du secteur. Le kit de développement logiciel (SDK) Windows Media format 11 comprend le codec Microsoft Windows Media Video 9 et le codec Microsoft Windows Media Audio 9,1. Ces deux codecs fournissent un encodage exceptionnel du contenu multimédia numérique. Nouveauté de cette version : le codec de profil avancé Windows Media Video 9, qui fournit des optimisations pour la diffusion vidéo. Ce kit de développement logiciel (SDK) comprend également le codec d’écran Microsoft Windows Media Video 9 permettant de compresser l’activité de l’écran de l’ordinateur pendant les sessions des applications de l’utilisateur, ainsi que le codec vocal Windows Media Audio 9,1, qui encode les données audio de faible complexité, telles que la parole et s’adapte intelligemment à un son plus complexe, par exemple la musique
-   Prise en charge de l’écriture de fichiers ASF. Les fichiers sont créés en fonction de profils personnalisables, ce qui facilite la configuration et la normalisation des fichiers. Ce kit de développement logiciel (SDK) peut être utilisé pour écrire des fichiers d’une capacité supérieure à 2 gigaoctets, ce qui permet d’obtenir des fichiers continus plus longs et de qualité.
-   Prise en charge de la lecture des fichiers ASF. Ce kit de développement logiciel (SDK) prend en charge la lecture des fichiers ASF locaux, ainsi que la lecture des données ASF diffusées en continu sur un réseau. La prise en charge est également fournie pour de nombreuses fonctionnalités de lecture avancées, telles que la prise en charge native des fichiers de débit binaire multiple (MBR), qui contiennent plusieurs flux avec le même contenu encodé à des vitesses de transmission différentes. Le lecteur sélectionne automatiquement le flux MBR à utiliser, en fonction de la bande passante disponible au moment de la lecture.
-   Prise en charge de la diffusion de flux ASF sur un réseau. Ce kit de développement logiciel (SDK) prend en charge la diffusion de données ASF via HTTP vers des ordinateurs distants sur un réseau, ainsi que la transmission de données directement à un serveur Windows Media distant.
-   Prise en charge de la modification des métadonnées dans les fichiers ASF. Les informations relatives à un fichier et son contenu sont manipulées facilement avec ce kit de développement logiciel (SDK). Les développeurs peuvent utiliser le système robuste d’attributs de métadonnées inclus dans le kit de développement logiciel (SDK), ou créer des attributs personnalisés en fonction de leurs besoins.
-   Prise en charge des applications de modification de contenu. Ce kit de développement logiciel (SDK) permet aux applications de rechercher des points dans un fichier par heure de présentation et par image vidéo. En outre, les fichiers créés à l’aide du kit de développement logiciel (SDK) du format Windows Media peuvent gérer les horodateurs dans les formats utilisés dans la production de films et de télévision.
-   Prise en charge de la lecture et de la modification des métadonnées dans les fichiers MP3. Ce kit de développement logiciel (SDK) fournit une prise en charge intégrée pour la lecture des fichiers MP3 avec les mêmes méthodes que celles utilisées pour lire les fichiers ASF. Les applications générées avec le kit de développement logiciel (SDK) Windows Media format peuvent également modifier les attributs de métadonnées dans les fichiers MP3 à l’aide de la prise en charge intégrée des balises ID3 les plus courantes utilisées par les créateurs de contenu.
-   Prise en charge de la protection Rights Management numérique. Ce kit de développement logiciel (SDK) fournit des méthodes pour lire et écrire des fichiers ASF et des flux réseau protégés par des Rights Management numériques afin d’empêcher la lecture ou la copie non autorisée du contenu.

Pour télécharger le kit de développement logiciel (SDK) Windows Media format, consultez la page [Windows Media downloads](https://msdn.microsoft.com/windows/desktop/aa904949) sur le site Web de Microsoft.

Ce document décrit comment vous pouvez développer des applications multimédias numériques à l’aide du kit de développement logiciel (SDK) Windows Media format. Elle est divisée en sections suivantes.

> [!Note]  
> Bien que ce document contienne des informations sur la dernière version du kit de développement logiciel (SDK) Windows Media format, la plupart des fonctionnalités qu’il décrit sont prises en charge par les versions antérieures du kit de développement logiciel (SDK). Les pages de référence pour les méthodes, les fonctions, les structures et les énumérations du kit de développement logiciel (SDK) du format Windows Media incluent les exigences de version.

 



| Section                                                                                                          | Description                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du kit de développement logiciel (SDK) Windows Media format](about-the-windows-media-format-sdk.md)                                     | Fournit une vue d’ensemble et des informations générales que vous devez connaître avant de tenter de créer des applications.                                                                                  |
| [Guide de programmation](programming-guide.md)                                                                       | Fournit des instructions détaillées pour effectuer diverses tâches, telles que la lecture, l’écriture et l’indexation de fichiers, la protection des fichiers avec des Rights Management numériques, la diffusion en continu de données ASF sur un réseau, etc. |
| [Guide de référence de programmation](programming-reference.md)                                                               | Fournit des informations de référence pour les interfaces, les méthodes, les fonctions, les structures, les types énumération et les constantes relatives au format Windows Media.                                                     |
| [Interfaces de codec vidéo et Windows Media Audio](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Fournit des instructions pour Windows Media Audio l’utilisation directe des DMOs et Video codec Digital Media Objects ().                                                                                           |
| [*Glossaire*](wmformat-glossary.md)                                                                              | Définit les termes utilisés dans la documentation du kit de développement logiciel (SDK) Windows Media format.                                                                                                                                    |



 

 

 




