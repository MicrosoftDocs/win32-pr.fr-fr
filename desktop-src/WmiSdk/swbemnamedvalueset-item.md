---
description: La méthode Item de l’objet SWbemNamedValueSet obtient un objet SWbemNamedValue de la collection.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: SWbemNamedValueSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528479"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="6491c-103">SWbemNamedValueSet. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="6491c-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="6491c-104">La méthode **Item** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) obtient un objet [**SWbemNamedValue**](swbemnamedvalue.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="6491c-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="6491c-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6491c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6491c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6491c-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6491c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6491c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6491c-108">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6491c-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6491c-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6491c-109">Required.</span></span> <span data-ttu-id="6491c-110">Nom de la valeur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6491c-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6491c-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6491c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6491c-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6491c-112">Reserved.</span></span> <span data-ttu-id="6491c-113">Cette valeur doit être égale à zéro si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6491c-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6491c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6491c-114">Return value</span></span>

<span data-ttu-id="6491c-115">En cas de réussite, l’objet [**SWbemNamedValue**](swbemnamedvalue.md) demandé est retourné.</span><span class="sxs-lookup"><span data-stu-id="6491c-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6491c-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6491c-116">Error codes</span></span>

<span data-ttu-id="6491c-117">À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="6491c-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6491c-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6491c-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6491c-119">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6491c-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6491c-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6491c-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6491c-121">Un paramètre non valide a été spécifié ou l’espace de noms n’a pas pu être analysé.</span><span class="sxs-lookup"><span data-stu-id="6491c-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="6491c-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6491c-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6491c-123">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="6491c-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6491c-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="6491c-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="6491c-125">L'élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6491c-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6491c-126">Notes</span><span class="sxs-lookup"><span data-stu-id="6491c-126">Remarks</span></span>

<span data-ttu-id="6491c-127">Pour obtenir des exemples d’ajout et de récupération de valeurs nommées, consultez [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="6491c-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6491c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6491c-128">Requirements</span></span>



| <span data-ttu-id="6491c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6491c-129">Requirement</span></span> | <span data-ttu-id="6491c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6491c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6491c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6491c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6491c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6491c-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6491c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6491c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6491c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6491c-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6491c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="6491c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6491c-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6491c-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6491c-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6491c-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="6491c-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6491c-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6491c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6491c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6491c-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6491c-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6491c-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="6491c-141">CLSID</span></span><br/>                    | <span data-ttu-id="6491c-142">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6491c-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="6491c-143">IID</span><span class="sxs-lookup"><span data-stu-id="6491c-143">IID</span></span><br/>                      | <span data-ttu-id="6491c-144">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6491c-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="6491c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6491c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6491c-146">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="6491c-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




