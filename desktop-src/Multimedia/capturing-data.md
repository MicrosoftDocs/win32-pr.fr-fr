---
title: Capturer des données
description: Capturer des données
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capCaptureSequence macro)
- capFileSaveAs macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029564"
---
# <a name="capturing-data"></a><span data-ttu-id="32503-105">Capturer des données</span><span class="sxs-lookup"><span data-stu-id="32503-105">Capturing Data</span></span>

<span data-ttu-id="32503-106">L’exemple suivant utilise la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) pour démarrer la capture vidéo et la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) pour copier les données capturées à partir du fichier de capture dans le fichier NEWFILE.AVI.</span><span class="sxs-lookup"><span data-stu-id="32503-106">The following example uses the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro to start video capture and the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro to copy the captured data from the capture file to the file NEWFILE.AVI.</span></span>


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a><span data-ttu-id="32503-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32503-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32503-108">Utilisation de la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="32503-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




