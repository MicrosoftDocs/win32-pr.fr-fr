---
description: La propriété SWbemRefreshableItem. ObjectSet représente le jeu d’objets à actualiser.
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: SWbemRefreshableItem. ObjectSet, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321530"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="51703-103">SWbemRefreshableItem. ObjectSet, propriété</span><span class="sxs-lookup"><span data-stu-id="51703-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="51703-104">La propriété **SWbemRefreshableItem. ObjectSet** représente le jeu d’objets à actualiser.</span><span class="sxs-lookup"><span data-stu-id="51703-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="51703-105">La propriété **ObjectSet** est un énumérateur ou un élément de collection contenu dans un objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="51703-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="51703-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="51703-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="51703-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="51703-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51703-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51703-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="51703-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="51703-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="51703-110">Notes</span><span class="sxs-lookup"><span data-stu-id="51703-110">Remarks</span></span>

<span data-ttu-id="51703-111">Cette propriété a la **valeur null** , sauf si [**SWbemRefreshableItem. isset**](swbemrefreshableitem-isset.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="51703-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="51703-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51703-112">Requirements</span></span>



| <span data-ttu-id="51703-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51703-113">Requirement</span></span> | <span data-ttu-id="51703-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="51703-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51703-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51703-115">Minimum supported client</span></span><br/> | <span data-ttu-id="51703-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51703-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51703-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51703-117">Minimum supported server</span></span><br/> | <span data-ttu-id="51703-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51703-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51703-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="51703-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="51703-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51703-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="51703-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="51703-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="51703-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="51703-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="51703-123">DLL</span><span class="sxs-lookup"><span data-stu-id="51703-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51703-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51703-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="51703-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="51703-125">CLSID</span></span><br/>                    | <span data-ttu-id="51703-126">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="51703-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="51703-127">IID</span><span class="sxs-lookup"><span data-stu-id="51703-127">IID</span></span><br/>                      | <span data-ttu-id="51703-128">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="51703-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="51703-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51703-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51703-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="51703-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="51703-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="51703-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




