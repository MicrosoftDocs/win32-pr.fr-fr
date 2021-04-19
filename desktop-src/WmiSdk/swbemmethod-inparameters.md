---
description: La propriété Parameters de l’objet SWbemMethod est un objet SWbemObject dont les propriétés définissent les paramètres d’entrée de cette méthode.
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: SWbemMethod. Parameters, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.InParameters
- ISWbemMethod.InParameters
- ISWbemMethod.get_InParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8df897f876673f6b4afe875e718401ae4c217e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518169"
---
# <a name="swbemmethodinparameters-property"></a><span data-ttu-id="2f1d4-103">SWbemMethod. Parameters, propriété</span><span class="sxs-lookup"><span data-stu-id="2f1d4-103">SWbemMethod.InParameters property</span></span>

<span data-ttu-id="2f1d4-104">La propriété **Parameters** de l’objet [**SWbemMethod**](swbemmethod.md) est un objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-104">The **InParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span> <span data-ttu-id="2f1d4-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-105">This property is read-only.</span></span> <span data-ttu-id="2f1d4-106">Notez que les modifications apportées à cet objet ne sont pas reflétées dans la définition de méthode sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-106">Note that any changes that are made to this object are not reflected in the underlying method definition.</span></span>

<span data-ttu-id="2f1d4-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2f1d4-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="2f1d4-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2f1d4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1d4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f1d4-109">Syntax</span></span>


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="2f1d4-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2f1d4-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2f1d4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2f1d4-111">Remarks</span></span>

<span data-ttu-id="2f1d4-112">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2f1d4-112">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1d4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f1d4-113">Requirements</span></span>



| <span data-ttu-id="2f1d4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f1d4-114">Requirement</span></span> | <span data-ttu-id="2f1d4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f1d4-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1d4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f1d4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2f1d4-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f1d4-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f1d4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f1d4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2f1d4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f1d4-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f1d4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f1d4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f1d4-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f1d4-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f1d4-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2f1d4-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f1d4-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f1d4-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f1d4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2f1d4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f1d4-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f1d4-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2f1d4-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="2f1d4-126">CLSID</span></span><br/>                    | <span data-ttu-id="2f1d4-127">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="2f1d4-127">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="2f1d4-128">IID</span><span class="sxs-lookup"><span data-stu-id="2f1d4-128">IID</span></span><br/>                      | <span data-ttu-id="2f1d4-129">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="2f1d4-129">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="2f1d4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f1d4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1d4-131">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-131">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="2f1d4-132">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-132">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="2f1d4-133">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-133">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="2f1d4-134">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-134">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="2f1d4-135">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="2f1d4-135">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




