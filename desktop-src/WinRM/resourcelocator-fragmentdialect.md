---
title: ResourceLocator. FragmentDialect, propriété (WSManDisp. h)
description: Obtient ou définit le dialecte de langage pour un dialecte de fragment de ressource quand ResourceLocator est utilisé dans les opérations d’objet de session telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété FragmentDialect
- Windows Remote Management de la propriété FragmentDialect, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, propriété FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466686"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="56bb3-106">ResourceLocator. FragmentDialect, propriété</span><span class="sxs-lookup"><span data-stu-id="56bb3-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="56bb3-107">Obtient ou définit le dialecte de langage pour un *dialecte* de [*fragment*](windows-remote-management-glossary.md) de [*ressource*](windows-remote-management-glossary.md) quand [**ResourceLocator**](resourcelocator.md) est utilisé dans les opérations d’objet de [**session**](session.md) telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="56bb3-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="56bb3-108">Un fragment représente une propriété ou une partie d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="56bb3-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="56bb3-109">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="56bb3-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="56bb3-110">Le dialecte indique quel langage XML décrit le fragment au service qui implémente le [protocole WS-Management](ws-management-protocol.md) et reçoit la requête.</span><span class="sxs-lookup"><span data-stu-id="56bb3-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="56bb3-111">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="56bb3-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bb3-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56bb3-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="56bb3-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="56bb3-113">Property value</span></span>

<span data-ttu-id="56bb3-114">Chaîne XML qui identifie le langage utilisé dans la propriété [**FragmentPath**](resourcelocator-fragmentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="56bb3-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="56bb3-115">La chaîne de dialecte est par défaut la spécification XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="56bb3-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="56bb3-116">Pour plus d’informations, consultez [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="56bb3-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="56bb3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="56bb3-117">Remarks</span></span>

<span data-ttu-id="56bb3-118">[**IWSManResourceLocator :: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) est la propriété C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="56bb3-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="56bb3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56bb3-119">Requirements</span></span>



| <span data-ttu-id="56bb3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56bb3-120">Requirement</span></span> | <span data-ttu-id="56bb3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="56bb3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bb3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bb3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56bb3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56bb3-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="56bb3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bb3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56bb3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56bb3-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="56bb3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="56bb3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bb3-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56bb3-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56bb3-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="56bb3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56bb3-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56bb3-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="56bb3-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56bb3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="56bb3-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56bb3-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56bb3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="56bb3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56bb3-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56bb3-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56bb3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56bb3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bb3-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="56bb3-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





