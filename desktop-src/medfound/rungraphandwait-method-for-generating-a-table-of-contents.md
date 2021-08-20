---
description: Fonction RunGraphAndWait pour générer une table des matières
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: Fonction RunGraphAndWait pour générer une table des matières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107c92926b814ba1a63f71ba410ebd86c194a752fd53e8701eb85bd2a0d17f34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058254"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a>Fonction RunGraphAndWait pour générer une table des matières

La fonction suivante est une fonction d’assistance dans un exemple de programme présenté dans [génération automatique d’une table des matières](generating-a-table-of-contents-automatically.md).


```C++
HRESULT RunGraphAndWait(IGraphBuilder* pGraph)
{
   IMediaControl* pControl = NULL;
   HRESULT hr = pGraph->QueryInterface(IID_IMediaControl, (VOID**)&pControl);

   if(SUCCEEDED(hr))
   {
      hr = pControl->Run();

      if(SUCCEEDED(hr))
      {
         IMediaEvent* pEvent = NULL;
         hr = pControl->QueryInterface(IID_IMediaEvent, (VOID**)&pEvent);

         if(SUCCEEDED(hr))
         {
           long eventCode = 0;
           hr = pEvent->WaitForCompletion(INFINITE, &eventCode);
           pEvent->Release();
           pEvent = NULL;
         }
      }

      pControl->Release();
      pControl = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération automatique d’une table des matières](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



