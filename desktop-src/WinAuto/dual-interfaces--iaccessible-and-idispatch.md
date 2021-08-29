---
title: Deux interfaces IAccessible et IDispatch
description: Les développeurs de serveurs doivent fournir l’interface COM (Component Object Model) standard IDispatch pour leurs objets accessibles.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292252bb8445c5934d8f8dc596e0b4f0d1c0d65415ed45dceace3cccb537ddff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115542"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a>Interfaces doubles : IAccessible et IDispatch

Les développeurs de serveurs doivent fournir l’interface COM (Component Object Model) standard [**IDispatch**](idispatch-interface.md) pour leurs objets accessibles. l’interface IDispatch permet aux applications clientes écrites dans Microsoft Visual Basic et divers langages de script d’utiliser les méthodes et propriétés exposées par [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Étant donné qu’un objet accessible fournit l’accès à un objet indirectement par le biais de [IDispatch :: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) ou directement à **IAccessible**, il est dit d’avoir une interface double.

Lorsque les clients C/C++ récupèrent un pointeur d’interface IDispatch, les clients peuvent appeler [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour essayer de convertir le pointeur d’interface IDispatch en un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Pour appeler les méthodes **IAccessible** indirectement, les clients C/C++ appellent IDispatch :: Invoke. Pour améliorer les performances, appelez les méthodes **IAccessible** pour utiliser directement l’objet.

Pour obtenir la liste des ID de dispatch (DISPID) que **IDispatch** utilise pour identifier les méthodes et propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , consultez [annexe C : IAccessible DISPID](appendix-c--iaccessible-dispids.md).

> [!Note]  
> Sous la version 2,0 et les versions ultérieures de Microsoft Active Accessibility, les serveurs n’ont pas à implémenter entièrement les méthodes de [**IDispatch**](idispatch-interface.md) , mais ils peuvent simplement retourner E \_ NOTIMPL après l’initialisation des paramètres out, comme illustré dans l’exemple suivant.

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 