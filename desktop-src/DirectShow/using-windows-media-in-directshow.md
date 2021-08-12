---
description: utilisation du média Windows dans DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: utilisation du média Windows dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fea308943d4be732c75e774d3e0c3cb09ac7c6609a8399d2e6eca4666d99e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651085"
---
# <a name="using-windows-media-in-directshow"></a>utilisation du média Windows dans DirectShow

cette section explique comment utiliser DirectShow pour lire et écrire des fichiers ASF (Advanced Systems Format). les fichiers ASF contiennent généralement du contenu audio et vidéo encodé à l’aide des codecs Windows Media Audio et vidéo. Toutefois, ASF peut contenir n’importe quel type de données.

les filtres de DirectShow suivants prennent en charge la lecture et l’écriture de fichiers ASF :

-   [Filtre de lecteur ASF WM](wm-asf-reader-filter.md). Lit les fichiers ASF.
-   [Filtre d’enregistreur ASF WM](wm-asf-writer-filter.md). Fichiers ASF Wrties.
-   [filtre de Wrapper DMO](dmo-wrapper-filter.md). encapsule l’encodeur multimédia Windows et le décodeur DMOs.

### <a name="versions"></a>Versions

Le lecteur ASF WM et les filtres du writer WM ASF sont empaquetés dans la DLL nommée qasf.dll, et les filtres sont appelés « composants QASF ». ces filtres sont des wrappers pour le kit de développement logiciel (SDK) de Format multimédia Windows. la DLL (qasf.dll) a été publiée pour la première fois dans le sdk DirectX, mais elle a été mise à jour ultérieurement dans le kit de développement logiciel (sdk) Windows Media Format. Voici l’historique des versions des filtres QASF :

-   DirectShow 8,1 prend en charge Windows kit de développement logiciel (SDK) Media Format version 7,0.
-   DirectShow 9,0 prend en charge Windows kit de développement logiciel (SDK) Media Format version 7,1.
-   Windows XP Service Pack 2 prend en charge Windows kit de développement logiciel (SDK) Media Format 9.
-   Windows Vista prend en charge Windows kit de développement logiciel (SDK) Media Format 11.
-   Windows Le kit de développement logiciel (SDK) Media Format 9 et ultérieur contient les versions correspondantes de QASF.

pour accéder à la dernière version de QASF, téléchargez toujours le dernier kit de développement logiciel (SDK) Windows Media Format.

### <a name="legacy-windows-media-source-filter"></a>filtre Source du média de Windows hérité

dans Windows XP Service Pack 1 et versions antérieures, le filtre source par défaut pour les fichiers ASF (extensions de fichier. ASF,. wmv et. wma) est le [filtre de source de média Windows](windows-media-source-filter.md)obsolète. ce comportement a été maintenu pour garantir la compatibilité descendante avec les applications qui utilisaient le Lecteur Windows Media 6,4. Les nouvelles applications doivent utiliser les versions plus récentes de QASF, qui font du filtre du lecteur ASF WM le filtre par défaut pour la lecture des fichiers ASF.

pour plus d’informations sur la suite Windows Media des kits de développement logiciel, consultez la section [Audio et vidéo](../audio-and-video.md) de la bibliothèque msdn.

Cet article contient les rubriques suivantes :

-   [Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
-   [Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DirectShow](using-directshow.md)
</dt> </dl>

 

 
