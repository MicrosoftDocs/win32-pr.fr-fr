---
description: Vous pouvez utiliser les fonctions suivantes pour travailler avec les données de performances dans Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Fonctions des compteurs de performances pour Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68fa9b417f6db987110d03fc0c3c88a920adf8cd70cf0ff5f844f26c0ef5c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033519"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Fonctions des compteurs de performances pour Visual Basic

> [!IMPORTANT]
> Les fonctions décrites dans cette rubrique peuvent être modifiées ou non disponibles à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Vous pouvez utiliser les fonctions suivantes pour travailler avec les données de performances dans Visual Basic.

- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhVbAddCounter**](pdhvbaddcounter.md)
- [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
- [**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
- [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
- [**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
- [**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
- [**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
- [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
- [**PdhVbOpenLog**](pdhvbopenlog.md)
- [**PdhVbOpenQuery**](pdhvbopenquery.md)
- [**PdhVbUpdateLog**](pdhvbupdatelog.md)

> [!NOTE]
> Les `PdhVb***` fonctions fonctionnent sur une session par processus et ne sont pas thread-safe. Ces fonctions ne doivent être utilisées qu’à partir d’applications simples à thread unique.
