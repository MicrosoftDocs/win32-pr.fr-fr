---
title: Incrémentation du nombre de références du gestionnaire
description: Incrémentation du nombre de références du gestionnaire
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a990f2570fca0057156a39a955930cca2d71858
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368252"
---
# <a name="incrementing-the-handler-reference-count"></a>Incrémentation du nombre de références du gestionnaire

La méthode **AddRef** incrémente le décompte de références du gestionnaire de fichiers ou du gestionnaire de flux.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




