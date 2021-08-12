---
title: Récupération d’un service SDO
description: Récupération d’un service SDO
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f1ec3f8537cbf6e9a7be82f8152bc764a263093fe0ebeee46ed1499abfd346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618955"
---
# <a name="retrieving-a-service-sdo"></a>Récupération d’un service SDO

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008.

 

Le code suivant récupère un objet de données serveur (SDO) pour le serveur NPS (Network Policy Server).


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



## <a name="remarks"></a>Remarques

Vous devez effectuer l' [attachement](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) à un ordinateur avant de pouvoir appeler l’une des méthodes [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attachement à un ordinateur SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 