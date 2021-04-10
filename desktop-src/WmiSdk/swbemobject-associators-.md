---
description: La méthode Associatorsrs \_ de l’objet SWbemObject retourne une collection d’objets (classes ou instances) qui sont associés à l’objet actuel.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Méthode SWbemObject.Associators_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952683"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="1574f-103">SWbemObject. Associatorss, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="1574f-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="1574f-104">La méthode **associatorsrs \_** de l’objet [**SWbemObject**](swbemobject.md) retourne une collection d’objets (classes ou instances) qui sont associés à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="1574f-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="1574f-105">Ces objets retournés sont appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1574f-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="1574f-106">Cette méthode exécute la même fonction que les ASSOCIateurs de la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="1574f-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="1574f-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1574f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1574f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1574f-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1574f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1574f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1574f-110">*strAssocClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-111">Chaîne qui contient une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="1574f-111">String that contains an association class.</span></span> <span data-ttu-id="1574f-112">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe d’association spécifiée ou d’une classe dérivée de cette classe d’association.</span><span class="sxs-lookup"><span data-stu-id="1574f-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-113">*strResultClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-114">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="1574f-114">String that contains a class name.</span></span> <span data-ttu-id="1574f-115">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="1574f-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-116">*strResultRole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-117">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="1574f-117">String that contains a property name.</span></span> <span data-ttu-id="1574f-118">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source.</span><span class="sxs-lookup"><span data-stu-id="1574f-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="1574f-119">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="1574f-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-120">*strRole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-121">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="1574f-121">String that contains a property name.</span></span> <span data-ttu-id="1574f-122">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent participer à une association avec l’objet source dans lequel l’objet source joue un rôle particulier.</span><span class="sxs-lookup"><span data-stu-id="1574f-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="1574f-123">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="1574f-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-124">*bClassesOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-125">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="1574f-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="1574f-126">Il s’agit des classes auxquelles les instances de point de terminaison appartiennent.</span><span class="sxs-lookup"><span data-stu-id="1574f-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="1574f-127">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="1574f-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-128">*bSchemaOnly* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-129">Il s’agit d’une valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="1574f-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="1574f-130">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="1574f-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="1574f-131">Elle peut uniquement avoir la valeur **true** si l’objet sur lequel cette méthode est appelée est une classe.</span><span class="sxs-lookup"><span data-stu-id="1574f-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="1574f-132">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont correctement associées à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="1574f-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-133">*strRequiredAssocQualifier* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-134">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="1574f-134">String that contains a qualifier name.</span></span> <span data-ttu-id="1574f-135">Ce paramètre, s’il est spécifié, indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1574f-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-136">*strRequiredQualifier* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-137">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="1574f-137">String that contains a qualifier name.</span></span> <span data-ttu-id="1574f-138">Ce paramètre, s’il est spécifié, indique que les points de terminaison retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1574f-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-139">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-140">Entier spécifiant des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="1574f-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="1574f-141">La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**, qui indique à l’appel qu’il doit retourner immédiatement plutôt que d’attendre la fin de la requête.</span><span class="sxs-lookup"><span data-stu-id="1574f-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="1574f-142">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1574f-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="1574f-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1574f-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1574f-144">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="1574f-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="1574f-145">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="1574f-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="1574f-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1574f-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1574f-147">Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="1574f-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="1574f-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1574f-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1574f-149">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="1574f-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="1574f-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1574f-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1574f-151">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="1574f-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="1574f-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1574f-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1574f-153">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="1574f-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="1574f-154">L’inclusion de cet indicateur rend le texte localisé du qualificateur de description disponible pour les classes, les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="1574f-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="1574f-155">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1574f-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1574f-156">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1574f-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1574f-157">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1574f-157">Typically, this is undefined.</span></span> <span data-ttu-id="1574f-158">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="1574f-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="1574f-159">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="1574f-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1574f-160">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1574f-160">Return value</span></span>

<span data-ttu-id="1574f-161">Si l’appel réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="1574f-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1574f-162">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1574f-162">Error codes</span></span>

<span data-ttu-id="1574f-163">À la fin de la méthode **associatorsrs \_** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="1574f-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="1574f-164">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="1574f-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="1574f-165">L’utilisateur actuel n’est pas autorisé à afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="1574f-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-166">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1574f-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1574f-167">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1574f-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-168">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1574f-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1574f-169">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1574f-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1574f-170">**wbemErrOutOfMemory** -2147749894</span><span class="sxs-lookup"><span data-stu-id="1574f-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="1574f-171">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1574f-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1574f-172">Notes</span><span class="sxs-lookup"><span data-stu-id="1574f-172">Remarks</span></span>

<span data-ttu-id="1574f-173">Pour plus d’informations sur les ASSOCIateurs de requêtes WQL, d’instances source et de points de terminaison associés, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="1574f-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1574f-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1574f-174">Requirements</span></span>



| <span data-ttu-id="1574f-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1574f-175">Requirement</span></span> | <span data-ttu-id="1574f-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="1574f-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1574f-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1574f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="1574f-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1574f-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1574f-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1574f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="1574f-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1574f-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1574f-181">En-tête</span><span class="sxs-lookup"><span data-stu-id="1574f-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="1574f-182"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1574f-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1574f-183">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1574f-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="1574f-184"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1574f-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1574f-185">DLL</span><span class="sxs-lookup"><span data-stu-id="1574f-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1574f-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1574f-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1574f-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="1574f-187">CLSID</span></span><br/>                    | <span data-ttu-id="1574f-188">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="1574f-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="1574f-189">IID</span><span class="sxs-lookup"><span data-stu-id="1574f-189">IID</span></span><br/>                      | <span data-ttu-id="1574f-190">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="1574f-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="1574f-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1574f-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1574f-192">**M**</span><span class="sxs-lookup"><span data-stu-id="1574f-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="1574f-193">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="1574f-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="1574f-194">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="1574f-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="1574f-195">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="1574f-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




