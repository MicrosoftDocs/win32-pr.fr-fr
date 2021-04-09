---
description: La méthode References \_ de l’objet SWbemObject retourne une collection de toutes les classes d’association ou instances qui font référence à l’objet actuel.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: Méthode SWbemObject.References_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868586"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="33dea-103">SWbemObject. References, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="33dea-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="33dea-104">La **méthode \_ References** de l’objet [**SWbemObject**](swbemobject.md) retourne une collection de toutes les classes d’association ou instances qui font référence à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="33dea-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="33dea-105">Cette méthode exécute la même fonction que les [références de](references-of-statement.md) la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="33dea-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="33dea-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="33dea-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="33dea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33dea-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="33dea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33dea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33dea-109">*strResultClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-110">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="33dea-110">String that contains a class name.</span></span> <span data-ttu-id="33dea-111">S’il est spécifié, ce paramètre indique que les objets d’association retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="33dea-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-112">*strRole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-113">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="33dea-113">String that contains a property name.</span></span> <span data-ttu-id="33dea-114">Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent être limités à ceux dans lesquels l’objet source joue un rôle spécifique.</span><span class="sxs-lookup"><span data-stu-id="33dea-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="33dea-115">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="33dea-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-116">*bClassesOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-117">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="33dea-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="33dea-118">Il s’agit des classes auxquelles appartiennent les objets Association.</span><span class="sxs-lookup"><span data-stu-id="33dea-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="33dea-119">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="33dea-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-120">*bSchemaOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-121">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="33dea-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="33dea-122">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="33dea-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="33dea-123">Elle peut uniquement avoir la valeur **true** si l’objet sur lequel cette méthode est appelée est une classe.</span><span class="sxs-lookup"><span data-stu-id="33dea-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="33dea-124">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="33dea-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-125">*strRequiredQualifier* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-126">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="33dea-126">String that contains a qualifier name.</span></span> <span data-ttu-id="33dea-127">S’il est spécifié, ce paramètre indique que les objets Association retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="33dea-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-128">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-129">Entier spécifiant des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="33dea-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="33dea-130">La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**, qui indique à l’appel qu’il doit retourner immédiatement plutôt que d’attendre la fin de la requête.</span><span class="sxs-lookup"><span data-stu-id="33dea-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="33dea-131">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="33dea-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="33dea-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="33dea-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="33dea-133">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="33dea-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="33dea-134">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="33dea-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="33dea-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="33dea-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="33dea-136">Fait en sorte que Windows Management Instrumentation (WMI) conserve des pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="33dea-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="33dea-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="33dea-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="33dea-138">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="33dea-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="33dea-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="33dea-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="33dea-140">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="33dea-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="33dea-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="33dea-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="33dea-142">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="33dea-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="33dea-143">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="33dea-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="33dea-144">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="33dea-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33dea-145">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="33dea-145">Typically, this is undefined.</span></span> <span data-ttu-id="33dea-146">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="33dea-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="33dea-147">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="33dea-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33dea-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33dea-148">Return value</span></span>

<span data-ttu-id="33dea-149">Si l’appel réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="33dea-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="33dea-150">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="33dea-150">Error codes</span></span>

<span data-ttu-id="33dea-151">Après l’achèvement de la **méthode \_ References** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="33dea-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="33dea-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="33dea-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="33dea-153">L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="33dea-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="33dea-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="33dea-155">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="33dea-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="33dea-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="33dea-157">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="33dea-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="33dea-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="33dea-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="33dea-159">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="33dea-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33dea-160">Notes</span><span class="sxs-lookup"><span data-stu-id="33dea-160">Remarks</span></span>

<span data-ttu-id="33dea-161">Pour plus d’informations sur les références des objets de requête WQL, d’instances source et d’association associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="33dea-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33dea-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33dea-162">Requirements</span></span>



| <span data-ttu-id="33dea-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33dea-163">Requirement</span></span> | <span data-ttu-id="33dea-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="33dea-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33dea-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33dea-165">Minimum supported client</span></span><br/> | <span data-ttu-id="33dea-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33dea-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33dea-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33dea-167">Minimum supported server</span></span><br/> | <span data-ttu-id="33dea-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33dea-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33dea-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="33dea-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="33dea-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33dea-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="33dea-171">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="33dea-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="33dea-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="33dea-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="33dea-173">DLL</span><span class="sxs-lookup"><span data-stu-id="33dea-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33dea-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33dea-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="33dea-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="33dea-175">CLSID</span></span><br/>                    | <span data-ttu-id="33dea-176">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="33dea-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="33dea-177">IID</span><span class="sxs-lookup"><span data-stu-id="33dea-177">IID</span></span><br/>                      | <span data-ttu-id="33dea-178">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="33dea-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="33dea-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33dea-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33dea-180">**M**</span><span class="sxs-lookup"><span data-stu-id="33dea-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="33dea-181">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="33dea-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="33dea-182">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="33dea-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="33dea-183">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="33dea-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




