---
description: La \_ méthode instances de l’objet SWbemObject crée un énumérateur qui retourne les instances de l’objet de classe actuel. Cette méthode implémente une requête simple. Les requêtes plus complexes peuvent nécessiter l’utilisation de SWbemServices.ExecQuery.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: Méthode SWbemObject.Instances_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523427"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="d904a-105">SWbemObject. instances, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="d904a-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="d904a-106">La **méthode \_ instances** de l’objet [**SWbemObject**](swbemobject.md) crée un énumérateur qui retourne les instances de l’objet de classe actuel.</span><span class="sxs-lookup"><span data-stu-id="d904a-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="d904a-107">Cette méthode implémente une requête simple.</span><span class="sxs-lookup"><span data-stu-id="d904a-107">This method implements a simple query.</span></span> <span data-ttu-id="d904a-108">Les requêtes plus complexes peuvent nécessiter l’utilisation de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="d904a-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="d904a-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d904a-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d904a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d904a-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d904a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d904a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d904a-112">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d904a-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d904a-113">Entier qui détermine le comportement de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d904a-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="d904a-114">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d904a-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="d904a-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d904a-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-116">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="d904a-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="d904a-117">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="d904a-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="d904a-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d904a-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-119">Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="d904a-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="d904a-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d904a-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-121">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d904a-121">Default value for this parameter.</span></span> <span data-ttu-id="d904a-122">Cet indicateur force l’appel à retourner immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d904a-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="d904a-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d904a-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-124">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="d904a-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="d904a-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d904a-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-126">Force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d904a-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="d904a-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d904a-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-128">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="d904a-128">Default for this parameter.</span></span> <span data-ttu-id="d904a-129">Cette valeur force l’énumération à inclure toutes les classes dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d904a-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d904a-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d904a-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d904a-131">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="d904a-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d904a-132">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d904a-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d904a-133">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="d904a-133">Typically, this is undefined.</span></span> <span data-ttu-id="d904a-134">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="d904a-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d904a-135">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="d904a-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d904a-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d904a-136">Return value</span></span>

<span data-ttu-id="d904a-137">Si la méthode réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) retourne.</span><span class="sxs-lookup"><span data-stu-id="d904a-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d904a-138">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d904a-138">Error codes</span></span>

<span data-ttu-id="d904a-139">Une fois la méthode **instances \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="d904a-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d904a-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d904a-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d904a-141">L’utilisateur actuel n’est pas autorisé à afficher les instances de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d904a-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="d904a-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d904a-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d904a-143">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d904a-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d904a-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="d904a-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d904a-145">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d904a-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d904a-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d904a-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d904a-147">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d904a-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d904a-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d904a-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d904a-149">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d904a-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d904a-150">Notes</span><span class="sxs-lookup"><span data-stu-id="d904a-150">Remarks</span></span>

<span data-ttu-id="d904a-151">La **méthode \_ instances** fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="d904a-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="d904a-152">Il n’y a pas d’erreur pour que la collection retournée n’ait aucun élément.</span><span class="sxs-lookup"><span data-stu-id="d904a-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="d904a-153">Le comportement par défaut de cette méthode est [*semi-synchrone*](gloss-s.md) en raison de la valeur *IFlags* par défaut **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="d904a-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d904a-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d904a-154">Requirements</span></span>



| <span data-ttu-id="d904a-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d904a-155">Requirement</span></span> | <span data-ttu-id="d904a-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d904a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d904a-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d904a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d904a-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d904a-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d904a-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d904a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d904a-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d904a-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d904a-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="d904a-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="d904a-162"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d904a-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d904a-163">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d904a-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="d904a-164"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d904a-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d904a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d904a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d904a-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d904a-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d904a-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="d904a-167">CLSID</span></span><br/>                    | <span data-ttu-id="d904a-168">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d904a-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d904a-169">IID</span><span class="sxs-lookup"><span data-stu-id="d904a-169">IID</span></span><br/>                      | <span data-ttu-id="d904a-170">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="d904a-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d904a-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d904a-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d904a-172">**M**</span><span class="sxs-lookup"><span data-stu-id="d904a-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="d904a-173">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="d904a-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




