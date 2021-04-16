---
description: Utilisation de Windows Media dans DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Utilisation de Windows Media dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393859"
---
# <a name="using-windows-media-in-directshow"></a>Utilisation de Windows Media dans DirectShow

Cette section décrit comment utiliser DirectShow pour lire et écrire des fichiers ASF (Advanced Systems Format). Les fichiers ASF contiennent généralement du contenu audio et vidéo encodé à l’aide des codecs Windows Media Audio et vidéo. Toutefois, ASF peut contenir n’importe quel type de données.

Les filtres DirectShow suivants prennent en charge la lecture et l’écriture de fichiers ASF :

-   [Filtre de lecteur ASF WM](wm-asf-reader-filter.md). Lit les fichiers ASF.
-   [Filtre d’enregistreur ASF WM](wm-asf-writer-filter.md). Fichiers ASF Wrties.
-   [Filtre de wrapper DMO](dmo-wrapper-filter.md). Encapsule le codeur et le décodeur Windows Media DMOs.

### <a name="versions"></a>Versions

Le lecteur ASF WM et les filtres du writer WM ASF sont empaquetés dans la DLL nommée qasf.dll, et les filtres sont appelés « composants QASF ». Ces filtres sont des wrappers pour le kit de développement logiciel (SDK) du format Windows Media. La DLL (qasf.dll) a été publiée pour la première fois dans le SDK DirectX, mais elle a été mise à jour ultérieurement dans le kit de développement logiciel (SDK) Windows Media format. Voici l’historique des versions des filtres QASF :

-   DirectShow 8,1 prend en charge le kit de développement logiciel (SDK) Windows Media format version 7,0.
-   DirectShow 9,0 prend en charge le kit de développement logiciel (SDK) Windows Media format version 7,1.
-   Windows XP Service Pack 2 prend en charge le kit de développement logiciel (SDK) Windows Media Format 9.
-   Windows Vista prend en charge le kit de développement logiciel (SDK) Windows Media format 11.
-   Le kit de développement logiciel (SDK) Windows Media Format 9 et versions ultérieures contiennent les versions correspondantes de QASF.

Pour accéder à la dernière version de QASF, téléchargez toujours le kit de développement logiciel (SDK) de format Windows Media le plus récent.

### <a name="legacy-windows-media-source-filter"></a>Filtre de source Windows Media hérité

Dans Windows XP Service Pack 1 et versions antérieures, le filtre source par défaut pour les fichiers ASF (extensions de fichier. ASF,. wmv et. WMA) est le [filtre de source Windows Media](windows-media-source-filter.md)obsolète. Ce comportement a été maintenu pour garantir la compatibilité descendante avec les applications qui utilisaient le lecteur Windows Media 6,4. Les nouvelles applications doivent utiliser les versions plus récentes de QASF, qui font du filtre du lecteur ASF WM le filtre par défaut pour la lecture des fichiers ASF.

Pour plus d’informations sur la suite Windows Media des kits de développement logiciel, consultez la section [audio et vidéo](../audio-and-video.md) de la bibliothèque MSDN.

Cet article contient les rubriques suivantes :

-   [Lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
-   [Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 
