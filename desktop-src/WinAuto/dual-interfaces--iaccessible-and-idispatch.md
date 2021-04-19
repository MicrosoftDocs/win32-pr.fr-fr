---
title: Deux interfaces IAccessible et IDispatch
description: Les développeurs de serveurs doivent fournir l’interface COM (Component Object Model) standard IDispatch pour leurs objets accessibles.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511075"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="83e18-103">Interfaces doubles : IAccessible et IDispatch</span><span class="sxs-lookup"><span data-stu-id="83e18-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="83e18-104">Les développeurs de serveurs doivent fournir l’interface COM (Component Object Model) standard [**IDispatch**](idispatch-interface.md) pour leurs objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="83e18-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="83e18-105">L’interface IDispatch permet aux applications clientes écrites dans Microsoft Visual Basic et divers langages de script d’utiliser les méthodes et propriétés exposées par [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="83e18-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="83e18-106">Étant donné qu’un objet accessible fournit l’accès à un objet indirectement par le biais de [IDispatch :: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) ou directement à **IAccessible**, il est dit d’avoir une interface double.</span><span class="sxs-lookup"><span data-stu-id="83e18-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="83e18-107">Lorsque les clients C/C++ récupèrent un pointeur d’interface IDispatch, les clients peuvent appeler [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour essayer de convertir le pointeur d’interface IDispatch en un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="83e18-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="83e18-108">Pour appeler les méthodes **IAccessible** indirectement, les clients C/C++ appellent IDispatch :: Invoke.</span><span class="sxs-lookup"><span data-stu-id="83e18-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="83e18-109">Pour améliorer les performances, appelez les méthodes **IAccessible** pour utiliser directement l’objet.</span><span class="sxs-lookup"><span data-stu-id="83e18-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="83e18-110">Pour obtenir la liste des ID de dispatch (DISPID) que **IDispatch** utilise pour identifier les méthodes et propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , consultez [annexe C : IAccessible DISPID](appendix-c--iaccessible-dispids.md).</span><span class="sxs-lookup"><span data-stu-id="83e18-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="83e18-111">Sous la version 2,0 et les versions ultérieures de Microsoft Active Accessibility, les serveurs n’ont pas à implémenter entièrement les méthodes de [**IDispatch**](idispatch-interface.md) , mais ils peuvent simplement retourner E \_ NOTIMPL après l’initialisation des paramètres out, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="83e18-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 