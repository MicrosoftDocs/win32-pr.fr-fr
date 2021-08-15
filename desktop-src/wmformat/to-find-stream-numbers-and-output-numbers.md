---
title: Pour rechercher les numéros de flux et les numéros de sortie
description: Pour rechercher les numéros de flux et les numéros de sortie
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- ASF (Advanced Systems Format), numéros de diffusion
- ASF (format des systèmes avancés), création de nombres
- ASF (Advanced Systems Format), recherche des numéros de sortie
- ASF (format des systèmes avancés), recherche des numéros de sortie
- lecteurs synchrones, numéros de flux
- lecteurs synchrones, recherche des numéros de sortie
- flux, recherche de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699587"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Pour rechercher les numéros de flux et les numéros de sortie

Le lecteur synchrone prend en charge un basculement plus simplifié entre le flux et les numéros de sortie pour la lecture que le lecteur asynchrone. Il est par conséquent plus important de savoir quels sont les nombres de flux qui correspondent aux numéros de sortie, ou l’inverse.

Pour rechercher le numéro de sortie qui correspond à un numéro de flux, appelez [**IWMSyncReader :: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Pour rechercher le numéro de flux qui correspond à un numéro de sortie, appelez [ **IWMSyncReader :: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




