---
title: Incrémentation du nombre de références du gestionnaire
description: Incrémentation du nombre de références du gestionnaire
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a990f2570fca0057156a39a955930cca2d71858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029698"
---
# <a name="incrementing-the-handler-reference-count"></a>Incrémentation du nombre de références du gestionnaire

La méthode **AddRef** incrémente le décompte de références du gestionnaire de fichiers ou du gestionnaire de flux.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




