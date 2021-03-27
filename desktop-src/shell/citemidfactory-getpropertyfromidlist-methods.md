---
description: Retourne une propriété à partir du IPropertyStore dans le IDList.
ms.assetid: D0BE2A9A-5832-4C0E-BFB6-96EB467C3D9D
title: CItemIDFactory::GetPropertyFromIDList methods (Shidfact.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 22aaec6d0616337a887f2876b51aaa744b205ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750277"
---
# <a name="citemidfactorygetpropertyfromidlist-methods"></a><span data-ttu-id="d5586-103">CItemIDFactory :: GetPropertyFromIDList, méthodes</span><span class="sxs-lookup"><span data-stu-id="d5586-103">CItemIDFactory::GetPropertyFromIDList methods</span></span>

<span data-ttu-id="d5586-104">Retourne une propriété à partir du [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dans le IDList.</span><span class="sxs-lookup"><span data-stu-id="d5586-104">Returns a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d5586-105">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="d5586-105">Overload list</span></span>



| <span data-ttu-id="d5586-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="d5586-106">Method</span></span>                                                                        | <span data-ttu-id="d5586-107">Description</span><span class="sxs-lookup"><span data-stu-id="d5586-107">Description</span></span>                                                                                                                                   |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5586-108">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="d5586-108">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span>     | <span data-ttu-id="d5586-109">Obtient une propriété à partir du [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dans le IDList en tant que variant, à l’aide de la clé.</span><span class="sxs-lookup"><span data-stu-id="d5586-109">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList as a variant, using the key.</span></span><br/>            |
| <span data-ttu-id="d5586-110">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="d5586-110">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span>    | <span data-ttu-id="d5586-111">Obtient une propriété à partir du [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dans le IDList en tant que variant, à l’aide de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d5586-111">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList as a variant, using the named property.</span></span><br/> |
| <span data-ttu-id="d5586-112">[**GetPropertyFromIDList**]/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist (pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="d5586-112">[**GetPropertyFromIDList**]/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span>  | <span data-ttu-id="d5586-113">Obtient une propriété à partir du [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dans le IDList, à l’aide de la clé.</span><span class="sxs-lookup"><span data-stu-id="d5586-113">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList, using the key.</span></span><br/>                         |
| <span data-ttu-id="d5586-114">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="d5586-114">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span> | <span data-ttu-id="d5586-115">Obtient une propriété à partir du [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) dans le IDList, à l’aide de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="d5586-115">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList, using the named property.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="d5586-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d5586-116">Requirements</span></span>



| <span data-ttu-id="d5586-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5586-117">Requirement</span></span> | <span data-ttu-id="d5586-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5586-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5586-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5586-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5586-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5586-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5586-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5586-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5586-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5586-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5586-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5586-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5586-124"><dt>Shidfact. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5586-124"><dt>Shidfact.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5586-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5586-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5586-126">**CItemIDFactory**</span><span class="sxs-lookup"><span data-stu-id="d5586-126">**CItemIDFactory**</span></span>](/windows/win32/api/shidfact/nl-shidfact-citemidfactory)
</dt> </dl>

 

 
