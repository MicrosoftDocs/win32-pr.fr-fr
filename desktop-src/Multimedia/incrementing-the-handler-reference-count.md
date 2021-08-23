---
title: Incrémentation du nombre de références du gestionnaire
description: Incrémentation du nombre de références du gestionnaire
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767efbd97525be49c0cf4604d2b90d068a2b81d78589627bf0654f3048e03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690589"
---
# <a name="incrementing-the-handler-reference-count"></a>Incrémentation du nombre de références du gestionnaire

La méthode **AddRef** incrémente le décompte de références du gestionnaire de fichiers ou du gestionnaire de flux.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




