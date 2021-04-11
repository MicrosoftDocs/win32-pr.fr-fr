---
title: Ajout d’un segment d’informations
description: Ajout d’un segment d’informations
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196918"
---
# <a name="adding-an-information-chunk"></a>Ajout d’un segment d’informations

Si vous devez inclure d’autres informations dans votre application en plus de l’audio et de la vidéo, vous pouvez créer des blocs d’informations et les insérer dans un fichier de capture. Les blocs d’informations peuvent contenir plusieurs types d’informations, notamment les détails d’une mention de droits d’auteur, l’identification de la source vidéo ou les informations de minutage externe. L’exemple suivant stocke les informations de temporisation externes d’un code temporel SMPTE (société de mouvement et ingénieurs de télévision) dans un segment d’informations et ajoute le segment à un fichier de capture à l’aide de la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




