---
description: Crée un énumérateur qui retourne les instances d’une classe spécifiée en fonction des critères de sélection spécifiés par l’utilisateur.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: SWbemServices. InstancesOf, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868570"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="9457c-103">SWbemServices. InstancesOf, méthode</span><span class="sxs-lookup"><span data-stu-id="9457c-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="9457c-104">La méthode **InstancesOf** de l’objet [**SWbemServices**](swbemservices.md) crée un énumérateur qui retourne les instances d’une classe spécifiée en fonction des critères de sélection spécifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9457c-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="9457c-105">Cette méthode implémente une requête simple.</span><span class="sxs-lookup"><span data-stu-id="9457c-105">This method implements a simple query.</span></span> <span data-ttu-id="9457c-106">Les requêtes plus complexes peuvent nécessiter l’utilisation de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="9457c-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="9457c-107">La méthode est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="9457c-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="9457c-108">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9457c-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9457c-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9457c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9457c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9457c-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9457c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9457c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9457c-112">*strClass*</span><span class="sxs-lookup"><span data-stu-id="9457c-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="9457c-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9457c-113">Required.</span></span> <span data-ttu-id="9457c-114">Chaîne qui contient le nom de la classe pour laquelle les instances sont souhaitées.</span><span class="sxs-lookup"><span data-stu-id="9457c-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="9457c-115">Ce paramètre ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="9457c-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="9457c-116">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9457c-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9457c-117">Ce paramètre détermine le détail que l’appel énumère et si cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9457c-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="9457c-118">La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="9457c-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="9457c-119">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9457c-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="9457c-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="9457c-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-121">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="9457c-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="9457c-122">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="9457c-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="9457c-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9457c-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-124">Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="9457c-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="9457c-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="9457c-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-126">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="9457c-126">Default value for this parameter.</span></span> <span data-ttu-id="9457c-127">Cet indicateur force l’appel à retourner immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9457c-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="9457c-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9457c-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-129">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="9457c-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="9457c-130">Cet indicateur appelle la méthode en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="9457c-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="9457c-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="9457c-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-132">Force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9457c-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="9457c-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9457c-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-134">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="9457c-134">Default value for this parameter.</span></span> <span data-ttu-id="9457c-135">Cette valeur force l’énumération à inclure toutes les classes dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="9457c-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9457c-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="9457c-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9457c-137">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="9457c-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="9457c-138">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="9457c-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9457c-139">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9457c-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9457c-140">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9457c-140">Typically, this is undefined.</span></span> <span data-ttu-id="9457c-141">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="9457c-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9457c-142">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="9457c-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9457c-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9457c-143">Return value</span></span>

<span data-ttu-id="9457c-144">En cas de réussite, la méthode retourne une [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="9457c-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="9457c-145">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9457c-145">Error codes</span></span>

<span data-ttu-id="9457c-146">À la fin de la méthode **InstancesOf** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="9457c-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="9457c-147">Un énumérateur retourné avec zéro élément n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="9457c-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="9457c-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9457c-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9457c-149">L’utilisateur actuel n’a pas l’autorisation d’afficher les instances de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9457c-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="9457c-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9457c-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9457c-151">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9457c-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9457c-152">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="9457c-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="9457c-153">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9457c-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9457c-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9457c-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9457c-155">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="9457c-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9457c-156">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9457c-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9457c-157">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="9457c-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9457c-158">Notes</span><span class="sxs-lookup"><span data-stu-id="9457c-158">Remarks</span></span>

<span data-ttu-id="9457c-159">La méthode **InstancesOf** fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="9457c-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="9457c-160">Par défaut, InstancesOf effectue une récupération complète.</span><span class="sxs-lookup"><span data-stu-id="9457c-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="9457c-161">Autrement dit, InstancesOf récupère toutes les instances de la ressource managée que vous identifiez et toutes les instances de toutes les sous-classes définies sous la classe cible.</span><span class="sxs-lookup"><span data-stu-id="9457c-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="9457c-162">Par exemple, le script suivant récupère toutes les ressources modélisées par toutes les classes dynamiques définies sous la \_ classe abstraite du service CIM.</span><span class="sxs-lookup"><span data-stu-id="9457c-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="9457c-163">Si vous exécutez ce script, vous obtiendrez des informations.</span><span class="sxs-lookup"><span data-stu-id="9457c-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="9457c-164">Toutefois, ces informations ne seront pas limitées aux services installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9457c-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="9457c-165">Au lieu de cela, elle inclut des informations de toutes les classes enfants du [**\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service), y compris [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) et [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9457c-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9457c-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9457c-166">Requirements</span></span>



| <span data-ttu-id="9457c-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9457c-167">Requirement</span></span> | <span data-ttu-id="9457c-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="9457c-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9457c-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9457c-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9457c-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9457c-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9457c-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9457c-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9457c-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9457c-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9457c-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="9457c-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9457c-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9457c-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9457c-175">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9457c-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="9457c-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9457c-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9457c-177">DLL</span><span class="sxs-lookup"><span data-stu-id="9457c-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9457c-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9457c-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9457c-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="9457c-179">CLSID</span></span><br/>                    | <span data-ttu-id="9457c-180">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="9457c-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="9457c-181">IID</span><span class="sxs-lookup"><span data-stu-id="9457c-181">IID</span></span><br/>                      | <span data-ttu-id="9457c-182">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="9457c-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9457c-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9457c-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9457c-184">**M**</span><span class="sxs-lookup"><span data-stu-id="9457c-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="9457c-185">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="9457c-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

