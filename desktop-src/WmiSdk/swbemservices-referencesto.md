---
description: Retourne une collection de toutes les classes d’association ou instances qui font référence à une classe ou une instance source spécifique.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: SWbemServices. ReferencesTo, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115798"
---
# <a name="swbemservicesreferencesto-method"></a><span data-ttu-id="20c81-103">SWbemServices. ReferencesTo, méthode</span><span class="sxs-lookup"><span data-stu-id="20c81-103">SWbemServices.ReferencesTo method</span></span>

<span data-ttu-id="20c81-104">La méthode **ReferencesTo** de l’objet [**SWbemServices**](swbemservices.md) retourne une collection de toutes les classes d’association ou instances qui font référence à une classe ou une instance source spécifique.</span><span class="sxs-lookup"><span data-stu-id="20c81-104">The **ReferencesTo** method of the [**SWbemServices**](swbemservices.md) object returns a collection of all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="20c81-105">Cette méthode exécute la même fonction que les [références de](references-of-statement.md) la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="20c81-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="20c81-106">Cette méthode est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="20c81-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="20c81-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="20c81-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="20c81-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="20c81-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20c81-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20c81-109">Syntax</span></span>


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="20c81-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20c81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c81-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="20c81-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="20c81-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="20c81-112">Required.</span></span> <span data-ttu-id="20c81-113">Chaîne qui contient le chemin d’accès de l’objet de la source pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="20c81-113">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="20c81-114">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="20c81-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="20c81-115">*strResultClass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-115">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-116">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="20c81-116">String that contains a class name.</span></span> <span data-ttu-id="20c81-117">Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent appartenir à la classe spécifiée dans ce paramètre ou en être dérivés.</span><span class="sxs-lookup"><span data-stu-id="20c81-117">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-118">*strRole* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-118">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-119">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="20c81-119">String that contains a property name.</span></span> <span data-ttu-id="20c81-120">Si ce paramètre est spécifié, ce paramètre indique que les objets d’association retournés doivent être limités à ceux dans lesquels l’objet source joue un rôle spécifique.</span><span class="sxs-lookup"><span data-stu-id="20c81-120">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="20c81-121">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="20c81-121">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-122">*bClassesOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-122">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-123">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="20c81-123">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="20c81-124">Il s’agit des classes auxquelles appartiennent les objets Association.</span><span class="sxs-lookup"><span data-stu-id="20c81-124">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="20c81-125">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="20c81-125">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-126">*bSchemaOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-126">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-127">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="20c81-127">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="20c81-128">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="20c81-128">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="20c81-129">Elle ne peut avoir la valeur **true** que si le paramètre *strObjectPath* spécifie le chemin d’accès à l’objet d’une classe.</span><span class="sxs-lookup"><span data-stu-id="20c81-129">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="20c81-130">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="20c81-130">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-131">*strRequiredQualifier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-131">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-132">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="20c81-132">String that contains a qualifier name.</span></span> <span data-ttu-id="20c81-133">S’il est spécifié, ce paramètre indique que les objets Association retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="20c81-133">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-134">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-134">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-135">Entier qui spécifie des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="20c81-135">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="20c81-136">La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**, qui indique à l’appel qu’il doit retourner immédiatement plutôt que d’attendre la fin de la requête.</span><span class="sxs-lookup"><span data-stu-id="20c81-136">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="20c81-137">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="20c81-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="20c81-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="20c81-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="20c81-139">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="20c81-139">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="20c81-140">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="20c81-140">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="20c81-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="20c81-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="20c81-142">Fait en sorte que Windows Management Instrumentation (WMI) conserve des pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="20c81-142">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="20c81-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="20c81-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="20c81-144">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="20c81-144">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="20c81-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="20c81-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="20c81-146">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="20c81-146">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="20c81-147">Cet indicateur appelle la méthode en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="20c81-147">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="20c81-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="20c81-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="20c81-149">Fait en sorte que WMI retourne des données de modification de classe avec la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="20c81-149">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="20c81-150">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="20c81-150">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="20c81-151">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="20c81-151">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20c81-152">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="20c81-152">Typically, this is undefined.</span></span> <span data-ttu-id="20c81-153">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="20c81-153">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="20c81-154">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="20c81-154">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c81-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20c81-155">Return value</span></span>

<span data-ttu-id="20c81-156">Si la méthode réussit, la méthode retourne un objet [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="20c81-156">If the method is successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20c81-157">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="20c81-157">Error codes</span></span>

<span data-ttu-id="20c81-158">À la fin de la méthode **ReferencesTo** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="20c81-158">After the completion of the **ReferencesTo** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="20c81-159">Une collection retournée avec zéro élément n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="20c81-159">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="20c81-160">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="20c81-160">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="20c81-161">L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="20c81-161">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="20c81-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="20c81-163">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="20c81-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-164">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="20c81-164">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="20c81-165">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="20c81-165">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-166">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="20c81-166">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="20c81-167">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="20c81-167">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="20c81-168">**wbemFlagUseAmendedQualifiers** -131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="20c81-168">**wbemFlagUseAmendedQualifiers** - 131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="20c81-169">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="20c81-169">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20c81-170">Notes</span><span class="sxs-lookup"><span data-stu-id="20c81-170">Remarks</span></span>

<span data-ttu-id="20c81-171">Pour plus d’informations sur les références des objets de requête WQL, d’instances source et d’association associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="20c81-171">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20c81-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20c81-172">Requirements</span></span>



| <span data-ttu-id="20c81-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20c81-173">Requirement</span></span> | <span data-ttu-id="20c81-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="20c81-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20c81-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c81-175">Minimum supported client</span></span><br/> | <span data-ttu-id="20c81-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20c81-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20c81-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20c81-177">Minimum supported server</span></span><br/> | <span data-ttu-id="20c81-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20c81-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20c81-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="20c81-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="20c81-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="20c81-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="20c81-181">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="20c81-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="20c81-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="20c81-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="20c81-183">DLL</span><span class="sxs-lookup"><span data-stu-id="20c81-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20c81-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20c81-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="20c81-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="20c81-185">CLSID</span></span><br/>                    | <span data-ttu-id="20c81-186">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="20c81-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="20c81-187">IID</span><span class="sxs-lookup"><span data-stu-id="20c81-187">IID</span></span><br/>                      | <span data-ttu-id="20c81-188">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="20c81-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="20c81-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c81-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c81-190">**M**</span><span class="sxs-lookup"><span data-stu-id="20c81-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="20c81-191">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="20c81-191">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="20c81-192">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="20c81-192">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="20c81-193">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="20c81-193">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> </dl>

 

 




