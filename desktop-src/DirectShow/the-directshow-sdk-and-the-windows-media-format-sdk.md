---
description: Le SDK DirectShow et le kit de développement logiciel (SDK) Windows Media format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Le SDK DirectShow et le kit de développement logiciel (SDK) Windows Media format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321641"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>Le SDK DirectShow et le kit de développement logiciel (SDK) Windows Media format

DirectShow et le kit de développement logiciel (SDK) du format Windows Media offrent des solutions complémentaires pour écrire des applications qui créent et lisent des flux de format Windows Media. Pour plus d’informations, consultez la section «[audio et vidéo](../audio-and-video.md)» de la bibliothèque MSDN.

Le filtre d’écriture ASF accepte un nombre quelconque de flux d’entrée et crée un fichier ASF. Le filtre utilise le kit de développement logiciel (SDK) Windows Media format pour convertir des fichiers audio ou vidéo non compressés en contenu Windows Media. Le contenu compressé est ensuite stocké dans le format de conteneur ASF. Si le contenu est uniquement audio, le fichier reçoit une extension. WMA et est appelé fichier Windows Media Audio. Si le contenu est vidéo uniquement ou vidéo et audio, le fichier reçoit une extension. wmv et est appelé fichier Windows Media Video. Chaque type de fichier peut également inclure des métadonnées.

Vous pouvez utiliser l’enregistreur ASF WM dans différents scénarios, y compris la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau. Ce filtre offre la seule façon de créer des fichiers Microsoft® Windows Media™ audio (WMA) et Windows Media Video (WMV) dans DirectShow®. Le filtre peut également créer des fichiers qui sont sécurisés par des Rights Management numériques (DRM) et peut également créer du contenu MPEG-4 à l’aide de l’encodeur Microsoft MPEG-4. Ce contenu est stocké dans le format de conteneur ASF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
