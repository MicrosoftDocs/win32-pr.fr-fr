---
title: Méthode ResourceLocator. ClearOptions (WSManDisp. h)
description: Supprime toutes les options de l’objet ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode ClearOptions
- Méthode ClearOptions Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843217"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="3c7ce-106">Méthode ResourceLocator. ClearOptions</span><span class="sxs-lookup"><span data-stu-id="3c7ce-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="3c7ce-107">Supprime toutes les [*options*](windows-remote-management-glossary.md) de l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="3c7ce-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="3c7ce-108">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="3c7ce-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c7ce-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c7ce-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="3c7ce-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c7ce-110">Parameters</span></span>

<span data-ttu-id="3c7ce-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c7ce-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3c7ce-112">Remarks</span></span>

<span data-ttu-id="3c7ce-113">**IWSManResourceLocator :: ClearOptions** est la méthode C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c7ce-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c7ce-114">Requirements</span></span>



| <span data-ttu-id="3c7ce-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c7ce-115">Requirement</span></span> | <span data-ttu-id="3c7ce-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c7ce-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7ce-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c7ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c7ce-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c7ce-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3c7ce-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c7ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c7ce-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c7ce-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3c7ce-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c7ce-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c7ce-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c7ce-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="3c7ce-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c7ce-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3c7ce-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c7ce-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c7ce-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c7ce-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3c7ce-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c7ce-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c7ce-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c7ce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c7ce-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="3c7ce-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





