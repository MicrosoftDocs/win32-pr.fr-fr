---
title: Utilisation de IADsExtension
description: Cette rubrique contient des exemples de code C++ pour l’utilisation de l’interface IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- extensions ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbab6813a87701fe2d7e130a03540476412c9e13b9d5d3ca96bdd0e63b2dad54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023487"
---
# <a name="iadsextension-usage"></a>Utilisation de IADsExtension

[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) est une interface facultative implémentée par le writer d’extension lorsqu’au moins l’une des conditions suivantes est remplie :

-   Le composant d’extension requiert une notification d’initialisation telle que définie par **ADSI \_ ext \_ * dwCode*** dans la méthode de [**fonctionnement**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .
-   L’extension prend en charge une interface double ou de dispatch.

Si un composant d’extension prend en charge l’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour la première raison, les méthodes [**IADsExtension ::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) et [**IADsExtension ::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) peuvent retourner **E \_ NOTIMPL**. En guise d’alternative, si un composant d’extension prend en charge une interface double ou de dispatch, la méthode de [**fonctionnement**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) peut ignorer les données et retourner un **HRESULT** de **E \_ NOTIMPL**.

Le code suivant illustre une extension qui implémente [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




