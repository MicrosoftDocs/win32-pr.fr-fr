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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367796"
---
# <a name="capturing-data"></a>Capturer des données

L’exemple suivant utilise la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) pour démarrer la capture vidéo et la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) pour copier les données capturées à partir du fichier de capture dans le fichier NEWFILE.AVI.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la capture vidéo](using-video-capture.md)
</dt> </dl>

 

 




