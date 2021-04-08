---
title: Obtention des ID enfants par les clients
description: Obtention des ID enfants par les clients
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727724"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="5dacb-103">Obtention des ID enfants par les clients</span><span class="sxs-lookup"><span data-stu-id="5dacb-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="5dacb-104">Les développeurs clients peuvent récupérer l’ID enfant d’un objet de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="5dacb-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="5dacb-105">Appelez [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span><span class="sxs-lookup"><span data-stu-id="5dacb-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="5dacb-106">Cette fonction récupère un tableau de structures de [**type Variant**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5dacb-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="5dacb-107">Interrogez l’objet pour voir s’il prend en charge l’interface [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="5dacb-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="5dacb-108">S’il est présent, utilisez [**IEnumVARIANT :: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtenir les ID enfants.</span><span class="sxs-lookup"><span data-stu-id="5dacb-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="5dacb-109">Collectez les ID enfants en appelant la méthode [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="5dacb-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="5dacb-110">Il incombe au client de libérer la mémoire utilisée pour les structures de [**variantes**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="5dacb-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="5dacb-111">Les clients doivent également appeler [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur toute interface [**IDispatch**](idispatch-interface.md) qui est retournée.</span><span class="sxs-lookup"><span data-stu-id="5dacb-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 