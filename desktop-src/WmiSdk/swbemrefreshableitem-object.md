---
description: La propriété SWbemRefreshableItem. Object représente une instance SWbemObject unique qui est actualisée. L’élément est contenu dans un objet SWbemRefresher. Instance SWbemObject qui est actualisée. L’élément est contenu dans un objet SWbemRefresher.
ms.assetid: 91a693c0-cde4-4cf6-b85a-662cfd0333e9
ms.tgt_platform: multiple
title: Propriété SWbemRefreshableItem. Object (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Object
- ISWbemRefreshableItem.Object
- ISWbemRefreshableItem.get_Object
- ISWbemRefreshableItem.put_Object
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b8456422088e9914562b87b2b114629bd80003c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953392"
---
# <a name="swbemrefreshableitemobject-property"></a><span data-ttu-id="bdf73-105">SWbemRefreshableItem. Object, propriété</span><span class="sxs-lookup"><span data-stu-id="bdf73-105">SWbemRefreshableItem.Object property</span></span>

<span data-ttu-id="bdf73-106">La propriété **SWbemRefreshableItem. Object** représente une instance [**SWbemObject**](swbemobject.md) unique qui est actualisée.</span><span class="sxs-lookup"><span data-stu-id="bdf73-106">The **SWbemRefreshableItem.Object** property represents a single [**SWbemObject**](swbemobject.md) instance that is refreshed.</span></span> <span data-ttu-id="bdf73-107">L’élément est contenu dans un objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="bdf73-107">The item is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="bdf73-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bdf73-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bdf73-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bdf73-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf73-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdf73-110">Syntax</span></span>


```VB
SWbemRefreshableItem.Object As Object
```



## <a name="property-value"></a><span data-ttu-id="bdf73-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bdf73-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf73-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bdf73-112">Remarks</span></span>

<span data-ttu-id="bdf73-113">Cette propriété a la **valeur null** , sauf si [**SWbemRefreshableItem. isset**](swbemrefreshableitem-isset.md) a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="bdf73-113">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf73-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdf73-114">Requirements</span></span>



| <span data-ttu-id="bdf73-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdf73-115">Requirement</span></span> | <span data-ttu-id="bdf73-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdf73-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf73-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdf73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf73-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdf73-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bdf73-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdf73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf73-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdf73-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bdf73-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdf73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf73-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf73-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdf73-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bdf73-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="bdf73-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bdf73-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bdf73-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bdf73-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdf73-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdf73-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bdf73-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="bdf73-127">CLSID</span></span><br/>                    | <span data-ttu-id="bdf73-128">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="bdf73-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="bdf73-129">IID</span><span class="sxs-lookup"><span data-stu-id="bdf73-129">IID</span></span><br/>                      | <span data-ttu-id="bdf73-130">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="bdf73-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="bdf73-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdf73-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf73-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="bdf73-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="bdf73-133">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="bdf73-133">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




