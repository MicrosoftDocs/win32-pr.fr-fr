---
title: Capturer des données
description: Capturer des données
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capCaptureSequence macro)
- capFileSaveAs macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764ff00dedcc044ed5234f8b647b08eaded35ce191bcb56e05cb35f47450677b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941297"
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

 

 




