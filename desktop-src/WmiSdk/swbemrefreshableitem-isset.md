---
description: La propriété SWbemRefreshableItem. IsSet est une valeur booléenne qui indique si l’objet SWbemRefreshableItem représente un objet unique ou un jeu d’objets. L’objet SWbemRefreshableItem représente un objet unique ou un jeu d’objets.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: SWbemRefreshableItem. IsSet, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106532356"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="f8a89-103">SWbemRefreshableItem. IsSet, propriété</span><span class="sxs-lookup"><span data-stu-id="f8a89-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="f8a89-104">La propriété **SWbemRefreshableItem. isset** est une valeur booléenne qui indique si l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) représente un objet unique ou un jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="f8a89-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="f8a89-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f8a89-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f8a89-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f8a89-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a89-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8a89-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f8a89-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f8a89-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a89-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f8a89-109">Remarks</span></span>

<span data-ttu-id="f8a89-110">Si **SWbemRefreshableItem. isset** a la **valeur true**, l’élément représente un objet [**SWbemObjectSet**](swbemobjectset.md) et la propriété de l' [**objet**](swbemrefreshableitem-object.md) est **null**.</span><span class="sxs-lookup"><span data-stu-id="f8a89-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="f8a89-111">Si la **valeur est false**, l’élément représente un objet [**SWbemObject**](swbemobject.md) et la propriété de l' **objet** est **null**.</span><span class="sxs-lookup"><span data-stu-id="f8a89-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a89-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8a89-112">Requirements</span></span>



| <span data-ttu-id="f8a89-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8a89-113">Requirement</span></span> | <span data-ttu-id="f8a89-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8a89-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a89-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8a89-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a89-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8a89-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8a89-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8a89-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a89-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8a89-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8a89-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8a89-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a89-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a89-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8a89-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f8a89-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8a89-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f8a89-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f8a89-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a89-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a89-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8a89-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f8a89-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="f8a89-125">CLSID</span></span><br/>                    | <span data-ttu-id="f8a89-126">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="f8a89-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="f8a89-127">IID</span><span class="sxs-lookup"><span data-stu-id="f8a89-127">IID</span></span><br/>                      | <span data-ttu-id="f8a89-128">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="f8a89-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="f8a89-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8a89-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a89-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="f8a89-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="f8a89-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="f8a89-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




