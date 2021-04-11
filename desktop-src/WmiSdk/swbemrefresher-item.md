---
description: La méthode SWbemRefresher. Item retourne le SWbemRefreshableItem spécifié à partir de la collection. SWbemRefreshableItem à partir de la collection.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: SWbemRefresher. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211238"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="9e7dc-103">SWbemRefresher. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="9e7dc-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="9e7dc-104">La méthode **SWbemRefresher. Item** retourne le [**SWbemRefreshableItem**](swbemrefreshableitem.md) spécifié à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="9e7dc-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9e7dc-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7dc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e7dc-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="9e7dc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e7dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7dc-108">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="9e7dc-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="9e7dc-109">Valeur d’index de l’élément dans la collection.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7dc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e7dc-110">Return value</span></span>

<span data-ttu-id="9e7dc-111">Si l’appel réussit, l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) spécifié est retourné.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9e7dc-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9e7dc-112">Error codes</span></span>

<span data-ttu-id="9e7dc-113">Si l’actualisateur n’a pas d’élément avec l’index spécifié, **wbemErrNotFound** est généré.</span><span class="sxs-lookup"><span data-stu-id="9e7dc-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7dc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e7dc-114">Requirements</span></span>



| <span data-ttu-id="9e7dc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e7dc-115">Requirement</span></span> | <span data-ttu-id="9e7dc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e7dc-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7dc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7dc-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e7dc-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e7dc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7dc-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e7dc-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e7dc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e7dc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e7dc-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7dc-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e7dc-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9e7dc-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e7dc-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e7dc-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e7dc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9e7dc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e7dc-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e7dc-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e7dc-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="9e7dc-127">CLSID</span></span><br/>                    | <span data-ttu-id="9e7dc-128">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="9e7dc-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="9e7dc-129">IID</span><span class="sxs-lookup"><span data-stu-id="9e7dc-129">IID</span></span><br/>                      | <span data-ttu-id="9e7dc-130">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="9e7dc-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="9e7dc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e7dc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7dc-132">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="9e7dc-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




