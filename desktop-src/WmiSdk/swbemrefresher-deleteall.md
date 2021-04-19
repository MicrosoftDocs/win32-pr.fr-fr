---
description: La méthode SWbemRefresher. DeleteAll supprime tous les éléments de la collection dans l’objet SWbemRefresher. Objet SWbemRefresher.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: SWbemRefresher. DeleteAll, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525792"
---
# <a name="swbemrefresherdeleteall-method"></a><span data-ttu-id="19492-103">SWbemRefresher. DeleteAll, méthode</span><span class="sxs-lookup"><span data-stu-id="19492-103">SWbemRefresher.DeleteAll method</span></span>

<span data-ttu-id="19492-104">La méthode **SWbemRefresher. DeleteAll** supprime tous les éléments de la collection dans l’objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="19492-104">The **SWbemRefresher.DeleteAll** method removes all the items from the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="19492-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="19492-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19492-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19492-106">Syntax</span></span>


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="19492-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19492-107">Parameters</span></span>

<span data-ttu-id="19492-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="19492-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19492-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19492-109">Return value</span></span>

<span data-ttu-id="19492-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="19492-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19492-111">Notes</span><span class="sxs-lookup"><span data-stu-id="19492-111">Remarks</span></span>

<span data-ttu-id="19492-112">La propriété d' [**actualisation**](swbemrefreshableitem-refresher.md) des [**SWbemRefreshableItem**](swbemrefreshableitem.md) correspondants pour chaque élément supprimé a la valeur **null**, ce qui indique qu’il n’a plus d’actualisation parente.</span><span class="sxs-lookup"><span data-stu-id="19492-112">The corresponding [**SWbemRefreshableItem**](swbemrefreshableitem.md) for each removed item has its [**Refresher**](swbemrefreshableitem-refresher.md) property set to **NULL**, which indicates that it no longer has a parent refresher.</span></span>

## <a name="requirements"></a><span data-ttu-id="19492-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19492-113">Requirements</span></span>



| <span data-ttu-id="19492-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19492-114">Requirement</span></span> | <span data-ttu-id="19492-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="19492-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19492-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19492-116">Minimum supported client</span></span><br/> | <span data-ttu-id="19492-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19492-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19492-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19492-118">Minimum supported server</span></span><br/> | <span data-ttu-id="19492-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19492-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19492-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="19492-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="19492-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="19492-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="19492-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="19492-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="19492-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19492-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19492-124">DLL</span><span class="sxs-lookup"><span data-stu-id="19492-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19492-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19492-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="19492-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="19492-126">CLSID</span></span><br/>                    | <span data-ttu-id="19492-127">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="19492-127">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="19492-128">IID</span><span class="sxs-lookup"><span data-stu-id="19492-128">IID</span></span><br/>                      | <span data-ttu-id="19492-129">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="19492-129">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="19492-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19492-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19492-131">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="19492-131">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




