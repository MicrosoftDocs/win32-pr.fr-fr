---
title: Récupération d’un service SDO
description: Récupération d’un service SDO
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afcea1885e0ed714587e99bc7c2dcd92f2fea422
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199304"
---
# <a name="retrieving-a-service-sdo"></a><span data-ttu-id="7b776-103">Récupération d’un service SDO</span><span class="sxs-lookup"><span data-stu-id="7b776-103">Retrieving a Service SDO</span></span>

> [!Note]  
> <span data-ttu-id="7b776-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7b776-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="7b776-105">Le code suivant récupère un objet de données serveur (SDO) pour le serveur NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="7b776-105">The following code retrieves a Server Data Object (SDO) for the Network Policy Server .</span></span>


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a><span data-ttu-id="7b776-106">Notes</span><span class="sxs-lookup"><span data-stu-id="7b776-106">Remarks</span></span>

<span data-ttu-id="7b776-107">Vous devez effectuer l' [attachement](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) à un ordinateur avant de pouvoir appeler l’une des méthodes [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="7b776-107">You must [attach](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) to a computer before you can call any of the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b776-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b776-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b776-109">Attachement à un ordinateur SDO-Enabled</span><span class="sxs-lookup"><span data-stu-id="7b776-109">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="7b776-110">**ISdoMachine::GetServiceSDO**</span><span class="sxs-lookup"><span data-stu-id="7b776-110">**ISdoMachine::GetServiceSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[<span data-ttu-id="7b776-111">**ISdoServiceControl**</span><span class="sxs-lookup"><span data-stu-id="7b776-111">**ISdoServiceControl**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 