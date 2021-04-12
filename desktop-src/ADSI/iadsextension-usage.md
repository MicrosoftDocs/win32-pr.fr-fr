---
title: Utilisation de IADsExtension
description: Cette rubrique contient des exemples de code C++ pour l’utilisation de l’interface IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- extensions ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190738"
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



 

 




