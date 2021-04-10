---
title: Récupération d’un utilisateur SDO
description: Récupération d’un utilisateur SDO
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c1d6320398afb4eed22f72f0c5e12495010323
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941170"
---
# <a name="retrieving-a-user-sdo"></a>Récupération d’un utilisateur SDO

Le code suivant récupère un objet de données serveur (SDO) pour l’administrateur.


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attachement à un ordinateur SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 