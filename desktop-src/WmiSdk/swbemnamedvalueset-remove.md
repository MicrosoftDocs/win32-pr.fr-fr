---
description: La méthode Remove de l’objet SWbemNamedValueSet supprime une valeur nommée du contexte.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: SWbemNamedValueSet. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540891"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="fadb2-103">SWbemNamedValueSet. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="fadb2-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="fadb2-104">La méthode **Remove** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) supprime une valeur nommée du contexte.</span><span class="sxs-lookup"><span data-stu-id="fadb2-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="fadb2-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fadb2-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fadb2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fadb2-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fadb2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fadb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fadb2-108">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fadb2-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fadb2-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fadb2-109">Required.</span></span> <span data-ttu-id="fadb2-110">Nom de la valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="fadb2-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="fadb2-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fadb2-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fadb2-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fadb2-112">Reserved.</span></span> <span data-ttu-id="fadb2-113">Cette valeur doit être égale à zéro si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fadb2-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fadb2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fadb2-114">Return value</span></span>

<span data-ttu-id="fadb2-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fadb2-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fadb2-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fadb2-116">Error codes</span></span>

<span data-ttu-id="fadb2-117">À la fin de la méthode **Remove** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="fadb2-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="fadb2-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fadb2-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fadb2-119">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fadb2-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fadb2-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="fadb2-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fadb2-121">Un paramètre non valide a été spécifié ou l’espace de noms n’a pas pu être analysé.</span><span class="sxs-lookup"><span data-stu-id="fadb2-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="fadb2-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="fadb2-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="fadb2-123">L'élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fadb2-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fadb2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fadb2-124">Requirements</span></span>



| <span data-ttu-id="fadb2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fadb2-125">Requirement</span></span> | <span data-ttu-id="fadb2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fadb2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fadb2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fadb2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fadb2-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fadb2-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fadb2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fadb2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fadb2-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fadb2-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fadb2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="fadb2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fadb2-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fadb2-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fadb2-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fadb2-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="fadb2-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fadb2-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fadb2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fadb2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fadb2-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fadb2-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fadb2-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="fadb2-137">CLSID</span></span><br/>                    | <span data-ttu-id="fadb2-138">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="fadb2-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="fadb2-139">IID</span><span class="sxs-lookup"><span data-stu-id="fadb2-139">IID</span></span><br/>                      | <span data-ttu-id="fadb2-140">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="fadb2-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="fadb2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fadb2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fadb2-142">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="fadb2-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




