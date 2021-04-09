---
title: ResourceLocator. MustUnderstandOptions, propriété (WSManDisp. h)
description: Obtient ou définit la valeur MustUnderstandOptions de l’objet ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété MustUnderstandOptions
- Windows Remote Management de la propriété MustUnderstandOptions, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, propriété MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942711"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="2fadc-106">ResourceLocator. MustUnderstandOptions, propriété</span><span class="sxs-lookup"><span data-stu-id="2fadc-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="2fadc-107">Obtient ou définit la valeur **MustUnderstandOptions** de l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="2fadc-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="2fadc-108">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="2fadc-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="2fadc-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2fadc-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fadc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fadc-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="2fadc-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2fadc-111">Property value</span></span>

<span data-ttu-id="2fadc-112">Indique, lorsque la **valeur est true**, que le service qui implémente l' [protocole WS-Management](ws-management-protocol.md) doit retourner une erreur s’il ne peut pas traiter l’option.</span><span class="sxs-lookup"><span data-stu-id="2fadc-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fadc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2fadc-113">Remarks</span></span>

<span data-ttu-id="2fadc-114">**IWSManResourceLocator :: MustUnderstandOptions** est la propriété C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="2fadc-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fadc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fadc-115">Requirements</span></span>



| <span data-ttu-id="2fadc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fadc-116">Requirement</span></span> | <span data-ttu-id="2fadc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fadc-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fadc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fadc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2fadc-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fadc-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2fadc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fadc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2fadc-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fadc-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2fadc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fadc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fadc-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fadc-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fadc-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="2fadc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fadc-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fadc-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2fadc-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2fadc-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fadc-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2fadc-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2fadc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2fadc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fadc-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fadc-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2fadc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fadc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fadc-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="2fadc-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





