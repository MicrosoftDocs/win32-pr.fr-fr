---
description: La propriété IsLocal de l’objet SWbemProperty est une valeur booléenne qui peut être utilisée pour déterminer si cette propriété est locale. La valeur FALSe indique que cette propriété a été héritée d’une autre classe. Cette propriété est en lecture seule.
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: SWbemProperty. IsLocal, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865657"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="e8808-105">SWbemProperty. IsLocal, propriété</span><span class="sxs-lookup"><span data-stu-id="e8808-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="e8808-106">La propriété **IsLocal** de l’objet [**SWbemProperty**](swbemproperty.md) est une valeur booléenne qui peut être utilisée pour déterminer si cette propriété est locale.</span><span class="sxs-lookup"><span data-stu-id="e8808-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="e8808-107">La valeur **false** indique que cette propriété a été héritée d’une autre classe.</span><span class="sxs-lookup"><span data-stu-id="e8808-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="e8808-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e8808-108">This property is read-only.</span></span>

<span data-ttu-id="e8808-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e8808-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e8808-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e8808-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8808-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8808-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e8808-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e8808-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="e8808-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8808-113">Requirements</span></span>



| <span data-ttu-id="e8808-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8808-114">Requirement</span></span> | <span data-ttu-id="e8808-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8808-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8808-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8808-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8808-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8808-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8808-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8808-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8808-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8808-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8808-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8808-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8808-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8808-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8808-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e8808-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8808-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8808-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8808-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e8808-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8808-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8808-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8808-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="e8808-126">CLSID</span></span><br/>                    | <span data-ttu-id="e8808-127">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="e8808-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="e8808-128">IID</span><span class="sxs-lookup"><span data-stu-id="e8808-128">IID</span></span><br/>                      | <span data-ttu-id="e8808-129">IID \_ ISWbemProperty</span><span class="sxs-lookup"><span data-stu-id="e8808-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




