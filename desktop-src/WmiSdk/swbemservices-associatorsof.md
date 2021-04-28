---
description: SWbemServices. AssociatorsOf, méthode-retourne une collection d’objets (classes ou instances) appelées points de terminaison associés à un objet spécifié.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: SWbemServices. AssociatorsOf, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 95dc8e16939c345b6f885980dd2f1194f180ac5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103687"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="da2b8-103">SWbemServices. AssociatorsOf, méthode</span><span class="sxs-lookup"><span data-stu-id="da2b8-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="da2b8-104">La méthode **AssociatorsOf** de l’objet [**SWbemServices**](swbemservices.md) retourne une collection d’objets (classes ou instances) appelées points de terminaison associés à un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="da2b8-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="da2b8-105">Cette méthode exécute la même fonction que les ASSOCIateurs de la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="da2b8-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="da2b8-106">Cette méthode est appelée par défaut en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="da2b8-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="da2b8-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="da2b8-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="da2b8-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="da2b8-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da2b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da2b8-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
  ByVal strObjectPath, _
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



## <a name="parameters"></a><span data-ttu-id="da2b8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da2b8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2b8-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="da2b8-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="da2b8-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="da2b8-112">Required.</span></span> <span data-ttu-id="da2b8-113">Chaîne qui contient le chemin d’accès de l’objet de la classe ou de l’instance source.</span><span class="sxs-lookup"><span data-stu-id="da2b8-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="da2b8-114">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="da2b8-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-115">*strAssocClass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-116">Chaîne qui contient une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="da2b8-116">String that contains an association class.</span></span> <span data-ttu-id="da2b8-117">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à la source par le biais de la classe d’association spécifiée ou d’une classe dérivée de cette classe d’association.</span><span class="sxs-lookup"><span data-stu-id="da2b8-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-118">*strResultClass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-119">Chaîne qui contient un nom de classe.</span><span class="sxs-lookup"><span data-stu-id="da2b8-119">String that contains a class name.</span></span> <span data-ttu-id="da2b8-120">S’il est spécifié, ce paramètre facultatif indique que les points de terminaison retournés doivent appartenir ou être dérivés de la classe spécifiée dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="da2b8-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-121">*strResultRole* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-122">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="da2b8-122">String that contains a property name.</span></span> <span data-ttu-id="da2b8-123">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent jouer un rôle particulier dans leur association avec l’objet source.</span><span class="sxs-lookup"><span data-stu-id="da2b8-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="da2b8-124">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="da2b8-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-125">*strRole* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-126">Chaîne qui contient un nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="da2b8-126">String that contains a property name.</span></span> <span data-ttu-id="da2b8-127">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent participer à une association avec l’objet source dans lequel l’objet source joue un rôle particulier.</span><span class="sxs-lookup"><span data-stu-id="da2b8-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="da2b8-128">Le rôle est défini par le nom d’une propriété spécifiée (qui doit être une propriété de référence) d’une association.</span><span class="sxs-lookup"><span data-stu-id="da2b8-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-129">*bClassesOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-130">Valeur booléenne qui indique si une liste de noms de classes doit être retournée plutôt que des instances réelles des classes.</span><span class="sxs-lookup"><span data-stu-id="da2b8-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="da2b8-131">Il s’agit des classes auxquelles les instances de point de terminaison appartiennent.</span><span class="sxs-lookup"><span data-stu-id="da2b8-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="da2b8-132">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="da2b8-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-133">*bSchemaOnly* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-134">Valeur booléenne qui indique si la requête s’applique au schéma plutôt qu’aux données.</span><span class="sxs-lookup"><span data-stu-id="da2b8-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="da2b8-135">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="da2b8-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="da2b8-136">Elle ne peut avoir la valeur **true** que si le paramètre *strObjectPath* spécifie le chemin d’accès à l’objet d’une classe.</span><span class="sxs-lookup"><span data-stu-id="da2b8-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="da2b8-137">Quand la valeur est **true**, le jeu de points de terminaison retournés représente des classes qui sont associées correctement à la classe source dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="da2b8-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-138">*strRequiredAssocQualifier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-139">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="da2b8-139">String that contains a qualifier name.</span></span> <span data-ttu-id="da2b8-140">Si ce paramètre est spécifié, ce paramètre indique que les points de terminaison retournés doivent être associés à l’objet source par le biais d’une classe d’association qui inclut le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="da2b8-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-141">*strRequiredQualifier* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-142">Chaîne qui contient un nom de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="da2b8-142">String that contains a qualifier name.</span></span> <span data-ttu-id="da2b8-143">S’il est spécifié, ce paramètre indique que les points de terminaison retournés doivent inclure le qualificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="da2b8-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-144">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-145">Entier qui spécifie des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="da2b8-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="da2b8-146">La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**, qui appelle la méthode en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="da2b8-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="da2b8-147">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="da2b8-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="da2b8-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="da2b8-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="da2b8-149">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="da2b8-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="da2b8-150">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="da2b8-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="da2b8-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="da2b8-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="da2b8-152">Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="da2b8-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="da2b8-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="da2b8-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="da2b8-154">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="da2b8-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="da2b8-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="da2b8-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="da2b8-156">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="da2b8-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="da2b8-157">Cet indicateur appelle la méthode en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="da2b8-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="da2b8-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="da2b8-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="da2b8-159">Fait en sorte que WMI retourne des données de modification de classe avec la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="da2b8-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="da2b8-160">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="da2b8-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="da2b8-161">*objwbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="da2b8-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-162">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="da2b8-162">Typically, this is undefined.</span></span> <span data-ttu-id="da2b8-163">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="da2b8-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="da2b8-164">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="da2b8-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2b8-165">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da2b8-165">Return value</span></span>

<span data-ttu-id="da2b8-166">Si l’appel réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="da2b8-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="da2b8-167">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="da2b8-167">Error codes</span></span>

<span data-ttu-id="da2b8-168">À la fin de la méthode **AssociatorsOf** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="da2b8-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="da2b8-169">Une collection retournée avec zéro élément n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="da2b8-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="da2b8-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="da2b8-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-171">L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="da2b8-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-172">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="da2b8-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-173">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="da2b8-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="da2b8-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-175">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="da2b8-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="da2b8-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-177">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="da2b8-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="da2b8-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="da2b8-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="da2b8-179">L’élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="da2b8-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da2b8-180">Notes </span><span class="sxs-lookup"><span data-stu-id="da2b8-180">Remarks</span></span>

<span data-ttu-id="da2b8-181">La méthode récupère les instances des ressources managées associées à une ressource spécifiée par le biais d’une ou plusieurs classes d’association.</span><span class="sxs-lookup"><span data-stu-id="da2b8-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="da2b8-182">Vous fournissez le chemin d’accès de l’objet pour le point de terminaison d’origine, et AssociatorsOf retourne les ressources managées au point de terminaison opposé.</span><span class="sxs-lookup"><span data-stu-id="da2b8-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="da2b8-183">La méthode AssociatorsOf exécute la même fonction que les ASSOCIateurs de la requête WQL.</span><span class="sxs-lookup"><span data-stu-id="da2b8-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="da2b8-184">Pour plus d’informations sur les ASSOCIateurs d’une requête WQL, d’instances source et de points de terminaison, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="da2b8-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da2b8-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da2b8-185">Requirements</span></span>



| <span data-ttu-id="da2b8-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da2b8-186">Requirement</span></span> | <span data-ttu-id="da2b8-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="da2b8-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da2b8-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da2b8-188">Minimum supported client</span></span><br/> | <span data-ttu-id="da2b8-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da2b8-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da2b8-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da2b8-190">Minimum supported server</span></span><br/> | <span data-ttu-id="da2b8-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da2b8-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da2b8-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="da2b8-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="da2b8-193"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2b8-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="da2b8-194">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="da2b8-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="da2b8-195"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da2b8-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da2b8-196">DLL</span><span class="sxs-lookup"><span data-stu-id="da2b8-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da2b8-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da2b8-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="da2b8-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="da2b8-198">CLSID</span></span><br/>                    | <span data-ttu-id="da2b8-199">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="da2b8-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="da2b8-200">IID</span><span class="sxs-lookup"><span data-stu-id="da2b8-200">IID</span></span><br/>                      | <span data-ttu-id="da2b8-201">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="da2b8-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="da2b8-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da2b8-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2b8-203">**M**</span><span class="sxs-lookup"><span data-stu-id="da2b8-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="da2b8-204">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="da2b8-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="da2b8-205">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="da2b8-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="da2b8-206">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="da2b8-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="da2b8-207">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="da2b8-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="da2b8-208">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="da2b8-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




