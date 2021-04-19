---
description: La propriété des paramètres de l’objet SWbemMethod est un objet SWbemObject dont les propriétés définissent les paramètres de sortie et le type de retour de cette méthode. Cette propriété est en lecture seule.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Propriété SWbemMethod. commeters (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530873"
---
# <a name="swbemmethodoutparameters-property"></a><span data-ttu-id="d666c-104">SWbemMethod. les paramètres de propriété</span><span class="sxs-lookup"><span data-stu-id="d666c-104">SWbemMethod.OutParameters property</span></span>

<span data-ttu-id="d666c-105">La propriété des **paramètres** de l’objet [**SWbemMethod**](swbemmethod.md) est un objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres de sortie et le type de retour de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d666c-105">The **OutParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span> <span data-ttu-id="d666c-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d666c-106">This property is read-only.</span></span>

<span data-ttu-id="d666c-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d666c-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d666c-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d666c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d666c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d666c-109">Syntax</span></span>


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="d666c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d666c-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d666c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d666c-111">Remarks</span></span>

<span data-ttu-id="d666c-112">Pour plus d’informations sur l’utilisation de cette propriété pour obtenir des paramètres de sortie à partir de méthodes de fournisseur, consultez [construction d’objets inparamètres et analyse d’objets de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md)de sortie.</span><span class="sxs-lookup"><span data-stu-id="d666c-112">For more information about how to use this property to obtain output parameters from provider methods, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="d666c-113">Notez que les modifications apportées à cet objet ne sont pas reflétées dans la définition de méthode sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="d666c-113">Note that any changes made to this object are not reflected in the underlying method definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="d666c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d666c-114">Requirements</span></span>



| <span data-ttu-id="d666c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d666c-115">Requirement</span></span> | <span data-ttu-id="d666c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d666c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d666c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d666c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d666c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d666c-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d666c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d666c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d666c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d666c-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d666c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d666c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d666c-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d666c-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d666c-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d666c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d666c-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d666c-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d666c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d666c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d666c-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d666c-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d666c-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="d666c-127">CLSID</span></span><br/>                    | <span data-ttu-id="d666c-128">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="d666c-128">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="d666c-129">IID</span><span class="sxs-lookup"><span data-stu-id="d666c-129">IID</span></span><br/>                      | <span data-ttu-id="d666c-130">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="d666c-130">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d666c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d666c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d666c-132">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="d666c-132">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="d666c-133">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="d666c-133">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="d666c-134">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d666c-134">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="d666c-135">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="d666c-135">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="d666c-136">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="d666c-136">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




