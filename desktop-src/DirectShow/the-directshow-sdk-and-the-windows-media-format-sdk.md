---
description: le sdk DirectShow et le kit de développement logiciel (sdk) Windows Media Format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: le sdk DirectShow et le kit de développement logiciel (sdk) Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651756"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>le sdk DirectShow et le kit de développement logiciel (sdk) Windows Media Format

DirectShow et le kit de développement logiciel (SDK) Windows Media format offrent des solutions complémentaires pour écrire des applications qui créent et lisent des flux de Windows media format. Pour plus d’informations, consultez la section «[audio et vidéo](../audio-and-video.md)» de la bibliothèque MSDN.

Le filtre d’écriture ASF accepte un nombre quelconque de flux d’entrée et crée un fichier ASF. le filtre utilise le kit de développement logiciel (SDK) de Format multimédia Windows pour convertir des fichiers audio ou vidéo non compressés en Windows contenu multimédia. Le contenu compressé est ensuite stocké dans le format de conteneur ASF. si le contenu est uniquement audio, le fichier reçoit une extension. wma et est appelé fichier Windows Media Audio. si le contenu est vidéo uniquement ou vidéo et audio, le fichier reçoit une extension. wmv et est appelé fichier Windows Media Video. Chaque type de fichier peut également inclure des métadonnées.

Vous pouvez utiliser l’enregistreur ASF WM dans différents scénarios, y compris la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau. ce filtre offre la seule façon de créer des fichiers Microsoft® Windows Media™ Audio (WMA) et Windows Media Video (WMV) dans DirectShow®. Le filtre peut également créer des fichiers qui sont sécurisés par des Rights Management numériques (DRM) et peut également créer du contenu MPEG-4 à l’aide de l’encodeur Microsoft MPEG-4. Ce contenu est stocké dans le format de conteneur ASF.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
