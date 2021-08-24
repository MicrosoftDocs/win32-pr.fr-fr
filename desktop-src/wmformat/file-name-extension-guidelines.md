---
title: Instructions relatives à l’extension de nom de fichier
description: Instructions relatives à l’extension de nom de fichier
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK, extensions de nom de fichier
- ASF (Advanced Systems Format), extensions de noms de fichiers
- ASF (format de systèmes avancés), extensions de nom de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ccd8c3b1b4ba27aa7360296fc336625cb0f51c4374bb77c06d349cb70a987c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704002"
---
# <a name="file-name-extension-guidelines"></a>Instructions relatives à l’extension de nom de fichier

Une extension de nom de fichier fournit à un éditeur de logiciels indépendant des informations sur les exigences de rendu d’une application qui utilise cette extension particulière.

l’extension de nom de fichier que vous devez utiliser pour un fichier créé par une application basée sur le kit de développement logiciel (SDK) Windows Media Format est déterminée par le type de contenu du fichier. Utilisez la logique suivante pour déterminer l’extension de nom de fichier que vous devez utiliser.

Si le fichier contient des flux encodés avec des codecs tiers ou des données non compressées non prises en charge (y compris des données arbitraires), le fichier doit utiliser l’extension. ASF.

si le fichier ne contient pas de flux non pris en charge et contient un ou plusieurs flux vidéo décompressés ou encodés avec n’importe quel Windows Media video codec, le fichier doit utiliser l’extension. wmv. ces fichiers peuvent également inclure des flux audio PCM, des flux audio encodés avec n’importe quel codec audio de média Windows, des flux de script et des flux Web.

si le fichier ne contient pas de flux non pris en charge et qu’aucun flux vidéo n’est pris en charge, et contient un ou plusieurs flux audio non compressés PCM ou encodés avec n’importe quel codec audio Windows Media, le fichier doit utiliser l’extension. wma. Ces fichiers peuvent également contenir des flux de script et des flux Web.

Si le fichier contient uniquement des flux qui ne sont ni des données audio ni des vidéos, il doit utiliser l’extension. ASF.

Les types de vidéo non compressés pris en charge sont RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU et YVU9.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Project Raisons**](project-considerations.md)
</dt> </dl>

 

 




