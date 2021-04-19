---
description: La méthode subclasss \_ de l’objet SWbemObject retourne un objet SWbemObjectSet.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: Méthode SWbemObject.Subclasses_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524972"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="f53ab-103">SWbemObject. Subclasses, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="f53ab-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="f53ab-104">La méthode **subclasss \_** de l’objet [**SWbemObject**](swbemobject.md) retourne un objet [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="f53ab-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="f53ab-105">Cet objet est une collection de sous-classes de l’objet actuel, qui doit être une classe.</span><span class="sxs-lookup"><span data-stu-id="f53ab-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="f53ab-106">Les éléments de la collection retournée peuvent être obtenus à l’aide de méthodes de collection standard.</span><span class="sxs-lookup"><span data-stu-id="f53ab-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="f53ab-107">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="f53ab-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="f53ab-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f53ab-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f53ab-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f53ab-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f53ab-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f53ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f53ab-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f53ab-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-112">Entier qui détermine le détail de l’énumération des appels.</span><span class="sxs-lookup"><span data-stu-id="f53ab-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="f53ab-113">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f53ab-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="f53ab-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f53ab-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f53ab-115">Force l’énumération récursive dans toutes les sous-classes dérivées de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f53ab-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="f53ab-116">La classe parent elle-même n’est pas retournée dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="f53ab-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="f53ab-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="f53ab-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f53ab-118">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f53ab-118">Default value for this parameter.</span></span> <span data-ttu-id="f53ab-119">Elle force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f53ab-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="f53ab-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="f53ab-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="f53ab-121">Provoque le retour immédiat de l’appel</span><span class="sxs-lookup"><span data-stu-id="f53ab-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="f53ab-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f53ab-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f53ab-123">Provoque le blocage de cet appel jusqu’à la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f53ab-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f53ab-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f53ab-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f53ab-125">Fait en sorte que WMI retourne des données de modification de classe avec la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="f53ab-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f53ab-126">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f53ab-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-127">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f53ab-127">Typically, this is undefined.</span></span> <span data-ttu-id="f53ab-128">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="f53ab-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f53ab-129">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="f53ab-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f53ab-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f53ab-130">Return value</span></span>

<span data-ttu-id="f53ab-131">Si l’appel réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="f53ab-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f53ab-132">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f53ab-132">Error codes</span></span>

<span data-ttu-id="f53ab-133">À la fin de la méthode **subclasss \_** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="f53ab-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f53ab-134">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="f53ab-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-135">L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="f53ab-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f53ab-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-137">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f53ab-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="f53ab-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-139">La classe spécifiée n’existait pas.</span><span class="sxs-lookup"><span data-stu-id="f53ab-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f53ab-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-141">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="f53ab-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f53ab-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-143">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f53ab-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f53ab-144">Notes</span><span class="sxs-lookup"><span data-stu-id="f53ab-144">Remarks</span></span>

<span data-ttu-id="f53ab-145">Il n’y a pas d’erreur pour que la collection retournée n’ait aucun élément, s’il n’existe aucune sous-classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="f53ab-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="f53ab-146">La méthode **subclasss \_** fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="f53ab-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53ab-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f53ab-147">Requirements</span></span>



| <span data-ttu-id="f53ab-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f53ab-148">Requirement</span></span> | <span data-ttu-id="f53ab-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="f53ab-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f53ab-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f53ab-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f53ab-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f53ab-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f53ab-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f53ab-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f53ab-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f53ab-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f53ab-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="f53ab-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f53ab-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f53ab-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f53ab-156">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f53ab-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="f53ab-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f53ab-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f53ab-158">DLL</span><span class="sxs-lookup"><span data-stu-id="f53ab-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f53ab-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f53ab-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f53ab-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="f53ab-160">CLSID</span></span><br/>                    | <span data-ttu-id="f53ab-161">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="f53ab-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f53ab-162">IID</span><span class="sxs-lookup"><span data-stu-id="f53ab-162">IID</span></span><br/>                      | <span data-ttu-id="f53ab-163">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="f53ab-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f53ab-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f53ab-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53ab-165">**M**</span><span class="sxs-lookup"><span data-stu-id="f53ab-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f53ab-166">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="f53ab-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




