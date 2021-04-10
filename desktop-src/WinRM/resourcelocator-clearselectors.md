---
title: Méthode ResourceLocator. ClearSelectors (WSManDisp. h)
description: Supprime tous les sélecteurs d’un objet ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode ClearSelectors
- Méthode ClearSelectors Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105628"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="25f9a-106">Méthode ResourceLocator. ClearSelectors</span><span class="sxs-lookup"><span data-stu-id="25f9a-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="25f9a-107">Supprime tous les [*sélecteurs*](windows-remote-management-glossary.md) d’un objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="25f9a-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="25f9a-108">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="25f9a-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="25f9a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25f9a-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="25f9a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25f9a-110">Parameters</span></span>

<span data-ttu-id="25f9a-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="25f9a-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f9a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="25f9a-112">Remarks</span></span>

<span data-ttu-id="25f9a-113">**IWSManResourceLocator :: ClearSelectors** est la méthode C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="25f9a-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f9a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25f9a-114">Requirements</span></span>



| <span data-ttu-id="25f9a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25f9a-115">Requirement</span></span> | <span data-ttu-id="25f9a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="25f9a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f9a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25f9a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25f9a-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25f9a-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="25f9a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25f9a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25f9a-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25f9a-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="25f9a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="25f9a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f9a-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f9a-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="25f9a-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="25f9a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25f9a-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25f9a-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="25f9a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25f9a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="25f9a-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25f9a-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25f9a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="25f9a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25f9a-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f9a-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25f9a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25f9a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f9a-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="25f9a-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





