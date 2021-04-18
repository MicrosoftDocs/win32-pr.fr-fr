---
description: Retourne un objet SWbemObjectPath qui contient le chemin d’accès de l’objet dans lequel les données ont été écrites.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: SWbemServicesEx. put, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519016"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="bfc49-103">SWbemServicesEx. put, méthode</span><span class="sxs-lookup"><span data-stu-id="bfc49-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="bfc49-104">La méthode **put** de l’objet [**SWbemServicesEx**](swbemservicesex.md) enregistre l’objet dans l’espace de noms lié à l’objet et retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui contient le chemin d’accès de l’objet dans lequel les données ont été écrites.</span><span class="sxs-lookup"><span data-stu-id="bfc49-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="bfc49-105">Cette méthode est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="bfc49-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="bfc49-106">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="bfc49-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="bfc49-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bfc49-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc49-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfc49-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bfc49-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfc49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc49-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="bfc49-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="bfc49-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bfc49-111">Required.</span></span> <span data-ttu-id="bfc49-112">Nouvel objet à placer dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="bfc49-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="bfc49-113">Il peut s’agir d’un objet nouvellement créé ou d’un objet modifié.</span><span class="sxs-lookup"><span data-stu-id="bfc49-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-114">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bfc49-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-115">Ce paramètre détermine si l’appel crée ou met à jour l’objet et si l’appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="bfc49-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="bfc49-116">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bfc49-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="bfc49-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="bfc49-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-118">Permet à une classe d’être mise à jour s’il n’y a pas de classes dérivées et qu’il n’existe aucune instance pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="bfc49-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="bfc49-119">Il autorise également les mises à jour dans tous les cas si la modification ne concerne que des qualificateurs peu importants (par exemple, le qualificateur de **Description** ).</span><span class="sxs-lookup"><span data-stu-id="bfc49-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="bfc49-120">Il s’agit du comportement par défaut pour cet appel et est utilisé pour la compatibilité avec les versions précédentes de WMI.</span><span class="sxs-lookup"><span data-stu-id="bfc49-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="bfc49-121">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="bfc49-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="bfc49-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="bfc49-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-123">Autorise les mises à jour des classes, même s’il existe des classes enfants, lorsque la modification n’entraîne pas de conflits avec les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="bfc49-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="bfc49-124">Vous pouvez utiliser cet indicateur lors de l’ajout d’une nouvelle propriété à une classe de base qui n’a pas été mentionnée précédemment dans une des classes enfants.</span><span class="sxs-lookup"><span data-stu-id="bfc49-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="bfc49-125">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="bfc49-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="bfc49-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="bfc49-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-127">Cet indicateur force les mises à jour des classes lorsque des classes enfants sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="bfc49-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="bfc49-128">Par exemple, cet indicateur force une mise à jour si un qualificateur de classe a été défini dans une classe enfant, et si la classe de base tente d’ajouter le même qualificateur en conflit avec l’identificateur existant.</span><span class="sxs-lookup"><span data-stu-id="bfc49-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="bfc49-129">En mode forcé, ce conflit est résolu en supprimant le qualificateur en conflit dans la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="bfc49-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="bfc49-130">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="bfc49-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="bfc49-131">L’utilisation du mode de force pour mettre à jour une classe statique entraîne la suppression de toutes les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="bfc49-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="bfc49-132">Une mise à jour forcée sur une classe de fournisseur ne supprime pas les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="bfc49-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="bfc49-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="bfc49-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-134">Provoque la création de la classe ou de l’instance si elle n’existe pas, ou si elle est remplacée si elle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="bfc49-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="bfc49-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="bfc49-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-136">Utilisé pour la création uniquement.</span><span class="sxs-lookup"><span data-stu-id="bfc49-136">Used for creation only.</span></span> <span data-ttu-id="bfc49-137">L’appel échoue si la classe ou l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="bfc49-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="bfc49-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="bfc49-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-139">Fait en sorte que cet appel effectue uniquement une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="bfc49-139">Causes this call to only do an update.</span></span> <span data-ttu-id="bfc49-140">La classe ou l’instance doit exister pour que l’appel réussisse.</span><span class="sxs-lookup"><span data-stu-id="bfc49-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="bfc49-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="bfc49-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-142">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bfc49-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="bfc49-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="bfc49-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-144">Entraîne le blocage de cet appel jusqu’à ce que l’opération soit terminée.</span><span class="sxs-lookup"><span data-stu-id="bfc49-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="bfc49-145">Cet indicateur appelle la méthode en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="bfc49-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="bfc49-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="bfc49-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="bfc49-147">Permet à WMI d’écrire des données de modification de classe ainsi que la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="bfc49-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="bfc49-148">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="bfc49-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bfc49-149">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bfc49-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-150">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="bfc49-150">Typically, this is undefined.</span></span> <span data-ttu-id="bfc49-151">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande.</span><span class="sxs-lookup"><span data-stu-id="bfc49-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="bfc49-152">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="bfc49-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc49-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfc49-153">Return value</span></span>

<span data-ttu-id="bfc49-154">Si l’appel réussit, un objet [**SWbemObjectPath**](swbemobjectpath.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="bfc49-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="bfc49-155">Cet objet contient le chemin d’accès à l’objet de l’instance ou de la classe qui a été correctement validée dans WMI.</span><span class="sxs-lookup"><span data-stu-id="bfc49-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bfc49-156">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bfc49-156">Error codes</span></span>

<span data-ttu-id="bfc49-157">Une fois la méthode **put** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="bfc49-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bfc49-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="bfc49-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-159">L’utilisateur actuel n’a pas l’autorisation pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="bfc49-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-160">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="bfc49-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-161">L’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="bfc49-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bfc49-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-163">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bfc49-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-164">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="bfc49-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-165">La valeur **null** a été spécifiée pour une propriété qui ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="bfc49-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="bfc49-166">Un exemple d’une telle propriété est une propriété marquée par un qualificateur de [**clé**](standard-qualifiers.md), **indexée** ou **not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="bfc49-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-167">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="bfc49-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-168">L’objet spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bfc49-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="bfc49-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-170">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bfc49-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-171">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="bfc49-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-172">L’indicateur **wbemChangeFlagUpdateOnly** a été spécifié, mais l’instance ou la classe n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="bfc49-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-173">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="bfc49-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-174">Les propriétés requises pour les classes n’ont pas toutes été définies.</span><span class="sxs-lookup"><span data-stu-id="bfc49-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="bfc49-175">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="bfc49-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bfc49-176">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bfc49-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfc49-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfc49-177">Requirements</span></span>



| <span data-ttu-id="bfc49-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfc49-178">Requirement</span></span> | <span data-ttu-id="bfc49-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfc49-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc49-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfc49-180">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc49-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfc49-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfc49-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfc49-182">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc49-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfc49-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfc49-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfc49-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc49-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc49-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfc49-186">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bfc49-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfc49-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bfc49-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bfc49-188">DLL</span><span class="sxs-lookup"><span data-stu-id="bfc49-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfc49-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfc49-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfc49-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="bfc49-190">CLSID</span></span><br/>                    | <span data-ttu-id="bfc49-191">CLSID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="bfc49-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="bfc49-192">IID</span><span class="sxs-lookup"><span data-stu-id="bfc49-192">IID</span></span><br/>                      | <span data-ttu-id="bfc49-193">IID \_ ISWbemServicesEx</span><span class="sxs-lookup"><span data-stu-id="bfc49-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




