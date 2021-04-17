---
title: Lecture des fichiers avec le lecteur asynchrone
description: Lecture des fichiers avec le lecteur asynchrone
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media Format SDK, lire des fichiers
- Windows Media Format SDK, lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- lecteurs asynchrones, interface IWMReaderCallback
- IWMReaderCallback, lecteurs asynchrones
- lecteurs asynchrones, lire des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381486"
---
# <a name="reading-files-with-the-asynchronous-reader"></a>Lecture des fichiers avec le lecteur asynchrone

Le lecteur asynchrone lit le contenu des fichiers ASF en utilisant plusieurs threads et appels asynchrones. Les fonctionnalités prises en charge par le lecteur asynchrone conviennent parfaitement aux applications qui assurent le rendu du contenu aux utilisateurs finaux.

Les fonctionnalités les plus basiques de l’objet lecteur peuvent être décomposées selon les étapes suivantes. Dans ces étapes, « l’application » fait référence au programme que vous écrivez à l’aide du kit de développement logiciel (SDK) du format Windows Media.

1.  L’application implémente l’interface [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pour gérer les messages à partir du lecteur. Cela comprend deux méthodes de rappel : **OnStatus**, qui reçoit les messages relatifs à l’état des différents aspects du lecteur et **OnSample**, qui reçoit des exemples non compressés du lecteur.
2.  L’application transmet au lecteur le nom d’un fichier à lire. Lorsque le lecteur ouvre le fichier, il attribue un numéro de sortie à chaque flux. Si le fichier utilise l’exclusion mutuelle, le lecteur assigne une seule sortie pour tous les flux qui s’excluent mutuellement.
3.  L’application obtient des informations sur la configuration des différentes sorties à partir du lecteur. Les informations collectées permettront à l’application de restituer correctement les exemples de supports.
4.  L’application demande au lecteur de commencer à lire les données à partir du fichier. Le lecteur commence à transmettre des échantillons non compressés au rappel **OnSample** un par un dans des mémoires tampons encapsulées dans des objets de mémoire tampon. Les exemples fournis par le lecteur sont dans l’ordre de la présentation. Le lecteur continue de fournir des échantillons jusqu’à ce qu’il soit arrêté par l’application ou jusqu’à ce que la fin du fichier soit atteinte.
5.  L’application est chargée du rendu des données une fois qu’elles sont fournies par le lecteur. Le kit de développement logiciel (SDK) Windows Media format ne fournit pas de routines de rendu. En règle générale, les applications utilisent d’autres kits de développement logiciel (SDK) pour restituer des données, telles que le kit de développement logiciel (SDK) Microsoft DirectX® ou les fonctions multimédias du kit SDK de plateforme Microsoft Windows.
6.  Lorsque la lecture est terminée, l’application demande au lecteur de fermer le fichier.

Ces étapes sont illustrées dans l’exemple d’application AudioPlayer, entre autres. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

Le lecteur prend également en charge des fonctionnalités plus avancées. Le lecteur vous permet d’effectuer les opérations suivantes :

-   Suspendre la lecture d’un fichier.
-   Récupérez les statistiques de performances des lecteurs.
-   Contrôle de la sélection de flux pour les flux mutuellement exclusifs.
-   Allouez manuellement les tampons pour la sortie.
-   Fournissez votre propre horloge.
-   Récupérez l’état des opérations sur les fichiers (mise en mémoire tampon, téléchargement ou enregistrement).
-   Ouvrez un fichier à l’aide de l’interface COM standard, **IStream**.
-   Recherchez des points spécifiques dans un fichier ASF.
-   Lire les données de profil dans l’en-tête du fichier.

Les sections suivantes décrivent en détail l’utilisation de l’objet Reader.

-   [Pour implémenter des messages de lecture dans le rappel OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [Pour implémenter le rappel OnSample](to-implement-the-onsample-callback.md)
-   [Pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md)
-   [Pour récupérer des exemples de médias avec le lecteur asynchrone](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [Pour effectuer une recherche par heure à l’aide du lecteur asynchrone](to-seek-by-time-using-the-asynchronous-reader.md)
-   [Pour rechercher par numéro de frame à l’aide du lecteur asynchrone](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur asynchrone](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [Pour rechercher des marqueurs](to-seek-to-markers.md)
-   [Pour suspendre ou arrêter la lecture](to-pause-or-stop-playback.md)
-   [Pour accéder aux statistiques de performances des lecteurs](to-get-reader-performance-statistics.md)
-   [Pour utiliser la sélection manuelle de flux](to-use-manual-stream-selection.md)
-   [Pour distribuer des exemples compressés avec le lecteur asynchrone](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Lecteur, objet**](reader-object.md)
</dt> </dl>

 

 




