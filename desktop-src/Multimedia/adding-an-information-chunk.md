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
# <a name="adding-an-information-chunk"></a><span data-ttu-id="7a3ac-104">Ajout d’un segment d’informations</span><span class="sxs-lookup"><span data-stu-id="7a3ac-104">Adding an Information Chunk</span></span>

<span data-ttu-id="7a3ac-105">Si vous devez inclure d’autres informations dans votre application en plus de l’audio et de la vidéo, vous pouvez créer des blocs d’informations et les insérer dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="7a3ac-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="7a3ac-106">Les blocs d’informations peuvent contenir plusieurs types d’informations, notamment les détails d’une mention de droits d’auteur, l’identification de la source vidéo ou les informations de minutage externe.</span><span class="sxs-lookup"><span data-stu-id="7a3ac-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="7a3ac-107">L’exemple suivant stocke les informations de temporisation externes d’un code temporel SMPTE (société de mouvement et ingénieurs de télévision) dans un segment d’informations et ajoute le segment à un fichier de capture à l’aide de la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="7a3ac-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7a3ac-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a3ac-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a3ac-109">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="7a3ac-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




