---
description: Fonction RunGraphAndWait pour générer une table des matières
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: Fonction RunGraphAndWait pour générer une table des matières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b71454bd8c47ab22f165ba59951037bf669a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201850"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a><span data-ttu-id="f6185-103">Fonction RunGraphAndWait pour générer une table des matières</span><span class="sxs-lookup"><span data-stu-id="f6185-103">RunGraphAndWait Function for Generating a Table of Contents</span></span>

<span data-ttu-id="f6185-104">La fonction suivante est une fonction d’assistance dans un exemple de programme présenté dans [génération automatique d’une table des matières](generating-a-table-of-contents-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="f6185-104">The following function is a helper function in an example program that is discussed in [Generating a Table of Contents Automatically](generating-a-table-of-contents-automatically.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f6185-105">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6185-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6185-106">Génération automatique d’une table des matières</span><span class="sxs-lookup"><span data-stu-id="f6185-106">Generating a Table of Contents Automatically</span></span>](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



