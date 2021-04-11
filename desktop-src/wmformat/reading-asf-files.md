---
title: Lecture des fichiers ASF
description: Lecture des fichiers ASF
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Media Format SDK, lire des fichiers ASF
- Windows Media Format SDK, ASF (Advanced Systems Format)
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f35cbd0e9a7dde800e23f83337ac30cdd66582
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311009"
---
# <a name="reading-asf-files"></a>Lecture des fichiers ASF

Le kit de développement logiciel (SDK) Windows Media format peut être utilisé pour fournir des exemples de supports à partir d’un fichier ASF. Deux objets sont utilisés pour récupérer des exemples, l’objet lecteur et l’objet lecteur synchrone.

L’objet lecteur est l’objet de lecture d’origine dans le kit de développement logiciel (SDK) de format Windows Media. L’objet lecteur utilise une architecture asynchrone pour envoyer des exemples à une application. Les applications générées à l’aide de l’objet Reader doivent implémenter des fonctions de rappel qui répondent aux divers messages et événements qui résultent de ce modèle multithread. Par souci de clarté, cette section fait référence à l’objet lecteur comme lecteur asynchrone.

L’objet lecteur synchrone est nouveau pour cette version du kit de développement logiciel (SDK) du format Windows Media. Le lecteur synchrone n’utilise pas plusieurs threads dans le traitement des exemples de fichiers ASF. Une application générée à l’aide du lecteur synchrone récupère des exemples à la demande, au lieu d’attendre que le lecteur les envoie.

Lorsque vous créez une application pour lire des fichiers ASF, vous devez choisir l’objet lecteur à utiliser. En général, les applications conçues pour fournir du contenu Windows Media doivent être créées à l’aide du lecteur asynchrone, tandis que les applications conçues pour modifier des fichiers ASF doivent être créées avec le lecteur synchrone.

Le tableau suivant répertorie les principales fonctionnalités des deux objets lecteur. Utilisez ce tableau pour déterminer l’objet à utiliser pour votre application.



| Fonctionnalité                                                                    | Lecteur Async | Lecteur de synchronisation |
|----------------------------------------------------------------------------|--------------|-------------|
| Lire les exemples non compressés par numéro de sortie                                 | Oui          | Oui         |
| Lire des exemples compressés par numéro de flux                                   | Oui          | Oui         |
| Lire des exemples non compressés par numéro de flux                                 | Non           | Oui         |
| Lire à partir d’un site Internet                                                    | Oui          | Non          |
| Lire les métadonnées                                                              | Oui          | Oui         |
| Rechercher l’heure de la présentation                                                  | Oui          | Oui         |
| Rechercher dans le frame                                                              | Oui          | Oui         |
| Rechercher dans le marqueur                                                             | Oui          | Non          |
| Basculer entre la remise compressée et l’exemple non compressé pendant la lecture | Non           | Oui         |
| Ouvrir des fichiers à l’aide de l’interface **IStream**                                     | Oui          | Oui         |



 

Les sections suivantes fournissent plus d’informations sur l’utilisation des deux objets Reader.



| Section                                                                                      | Description                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Utilisation des sorties](working-with-outputs.md)                                             | Décrit comment utiliser et manipuler des sorties. S’applique aux deux objets Reader.                                                            |
| [Allocation de tampons pour la lecture de fichiers](allocating-buffers-for-file-reading.md)               | Décrit comment utiliser votre propre pool de mémoires tampons pour contenir les exemples fournis par le lecteur ou le lecteur synchrone.                            |
| [Lecture des métadonnées lors de la lecture](reading-metadata-at-playback.md)                             | Décrit comment tirer parti de la prise en charge des métadonnées lors de la lecture. S’applique aux deux objets Reader.                                        |
| [Obtention d’informations de profil lors de la lecture](getting-profile-information-at-playback.md)       | Décrit comment accéder aux informations de profil pour les fichiers ouverts. S’applique aux deux objets Reader.                                           |
| [Lecture de l’audio multicanal](reading-multichannel-audio.md)                                 | Décrit comment configurer le writer pour décoder correctement l’audio multicanal.                                                            |
| [Rendu du contenu](rendering-content.md)                                                   | Décrit les problèmes liés au rendu d’exemples non compressés. S’applique aux deux objets Reader.                                         |
| [Obtenir les meilleures performances de recherche de vidéos](getting-the-best-video-seeking-performance.md) | Décrit les façons d’améliorer les performances de recherche de vidéos.                                                                                    |
| [Lecture des fichiers avec le lecteur asynchrone](reading-files-with-the-asynchronous-reader.md) | Décrit comment lire des fichiers ASF à l’aide de l’objet lecteur asynchrone.                                                                   |
| [Lecture des fichiers avec le lecteur synchrone](reading-files-with-the-synchronous-reader.md)   | Décrit comment lire des fichiers ASF à l’aide de l’objet lecteur synchrone.                                                                    |
| [Activation de l’accélération vidéo DirectX](enabling-directx-video-acceleration.md)               | Décrit comment implémenter l’accélération vidéo DirectX pour utiliser les fonctionnalités d’accélération matérielle de certaines cartes vidéo pour décoder la vidéo. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> <dt>

[**Lecteur, objet**](reader-object.md)
</dt> <dt>

[**Lecteur synchrone, objet**](synchronous-reader-object.md)
</dt> </dl>

 

 




