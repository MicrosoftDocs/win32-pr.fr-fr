---
description: La \_ méthode put de SWbemObject crée ou met à jour une instance ou un objet de classe pour Windows Management Instrumentation (WMI). Vous pouvez utiliser cette méthode après avoir modifié des propriétés ou des méthodes dans un SWbemObject, et vos modifications sont écrites dans WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: Méthode SWbemObject.Put_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533811"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="d858a-104">SWbemObject. put, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="d858a-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="d858a-105">La **méthode \_ put** de [**SWbemObject**](swbemobject.md) crée ou met à jour une instance ou un objet de classe pour Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d858a-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="d858a-106">Vous pouvez utiliser cette méthode après avoir modifié des propriétés ou des méthodes dans un **SWbemObject**, et vos modifications sont écrites dans WMI.</span><span class="sxs-lookup"><span data-stu-id="d858a-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="d858a-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d858a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d858a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d858a-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d858a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d858a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d858a-110">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d858a-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d858a-111">Ce paramètre détermine si l’appel crée ou met à jour la classe ou l’instance et si l’appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d858a-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="d858a-112">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d858a-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="d858a-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d858a-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-114">Permet à une classe d’être mise à jour s’il n’y a pas de classes dérivées et qu’il n’existe aucune instance pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="d858a-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="d858a-115">Il autorise également les mises à jour dans tous les cas si la modification concerne uniquement des qualificateurs peu importants (par exemple, le qualificateur de **Description** ).</span><span class="sxs-lookup"><span data-stu-id="d858a-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="d858a-116">Il s’agit du comportement par défaut pour cet appel et est utilisé pour la compatibilité avec les versions précédentes de WMI.</span><span class="sxs-lookup"><span data-stu-id="d858a-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="d858a-117">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="d858a-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="d858a-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d858a-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-119">Autorise les mises à jour des classes, même s’il existe des classes enfants si la modification n’entraîne pas de conflits avec les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="d858a-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="d858a-120">Vous pouvez utiliser cet indicateur lors de l’ajout d’une nouvelle propriété à une classe de base qui n’a pas été mentionnée précédemment dans une des classes enfants.</span><span class="sxs-lookup"><span data-stu-id="d858a-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="d858a-121">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="d858a-121">If the class has instances the update fails.</span></span> <span data-ttu-id="d858a-122">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="d858a-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="d858a-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="d858a-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-124">Cet indicateur force les mises à jour des classes lorsque des classes enfants sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="d858a-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="d858a-125">Par exemple, cet indicateur force une mise à jour si un qualificateur de classe a été défini dans une classe enfant, et si la classe de base tente d’ajouter le même qualificateur et en conflit avec l’option existante.</span><span class="sxs-lookup"><span data-stu-id="d858a-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="d858a-126">En mode de forçage, ce conflit serait résolu en supprimant le qualificateur en conflit dans la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="d858a-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="d858a-127">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="d858a-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="d858a-128">L’utilisation du mode force pour mettre à jour une classe statique entraîne la suppression de toutes les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d858a-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="d858a-129">Une mise à jour forcée sur une classe de fournisseur ne supprime pas les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="d858a-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="d858a-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d858a-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-131">Provoque la création de la classe ou de l’instance si elle n’existe pas ou est remplacée si elle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d858a-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="d858a-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="d858a-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-133">Utilisé pour la création uniquement.</span><span class="sxs-lookup"><span data-stu-id="d858a-133">Used for creation only.</span></span> <span data-ttu-id="d858a-134">L’appel échoue si la classe ou l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d858a-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="d858a-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d858a-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-136">Provoque la mise à jour de cet appel.</span><span class="sxs-lookup"><span data-stu-id="d858a-136">Causes this call to update.</span></span> <span data-ttu-id="d858a-137">La classe ou l’instance doit exister pour que l’appel réussisse.</span><span class="sxs-lookup"><span data-stu-id="d858a-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="d858a-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d858a-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-139">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d858a-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="d858a-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d858a-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-141">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="d858a-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d858a-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d858a-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d858a-143">Permet à WMI d’écrire des données de modification de classe ainsi que la définition de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="d858a-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="d858a-144">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="d858a-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d858a-145">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d858a-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d858a-146">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="d858a-146">Typically, this is undefined.</span></span> <span data-ttu-id="d858a-147">Dans le cas contraire, il s’agit d’un objet [**SWbemObjectPath**](swbemobjectpath.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="d858a-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d858a-148">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="d858a-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d858a-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d858a-149">Return value</span></span>

<span data-ttu-id="d858a-150">Si l’appel réussit, un objet [**SWbemObjectPath**](swbemobjectpath.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="d858a-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="d858a-151">Cet objet contient le chemin d’accès à l’objet de l’instance ou de la classe qui a été correctement validée dans WMI.</span><span class="sxs-lookup"><span data-stu-id="d858a-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d858a-152">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d858a-152">Error codes</span></span>

<span data-ttu-id="d858a-153">Une fois la méthode **put \_** terminée, l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="d858a-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d858a-154">**wbemErrAccessDenied** -2147749891</span><span class="sxs-lookup"><span data-stu-id="d858a-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="d858a-155">L’utilisateur actuel n’est pas autorisé à mettre à jour une instance de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d858a-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-156">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="d858a-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-157">L’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d858a-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-158">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d858a-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-159">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d858a-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-160">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="d858a-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-161">La valeur **Nothing** a été spécifiée pour une propriété qui ne peut pas être **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="d858a-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="d858a-162">Un exemple d’une telle propriété est une propriété marquée par un qualificateur de **clé,** **indexée** ou **not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="d858a-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-163">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="d858a-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-164">L'instance spécifiée n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d858a-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-165">**wbemErrInvalidParameter** -0x80041008</span><span class="sxs-lookup"><span data-stu-id="d858a-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="d858a-166">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d858a-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-167">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d858a-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-168">L’indicateur **wbemChangeFlagUpdateOnly** a été spécifié, mais l’instance ou la classe n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d858a-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-169">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="d858a-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-170">Les propriétés requises pour les classes n’ont pas toutes été définies.</span><span class="sxs-lookup"><span data-stu-id="d858a-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="d858a-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d858a-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d858a-172">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d858a-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d858a-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d858a-173">Requirements</span></span>



| <span data-ttu-id="d858a-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d858a-174">Requirement</span></span> | <span data-ttu-id="d858a-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="d858a-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d858a-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d858a-176">Minimum supported client</span></span><br/> | <span data-ttu-id="d858a-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d858a-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d858a-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d858a-178">Minimum supported server</span></span><br/> | <span data-ttu-id="d858a-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d858a-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d858a-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="d858a-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="d858a-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d858a-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d858a-182">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d858a-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="d858a-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d858a-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d858a-184">DLL</span><span class="sxs-lookup"><span data-stu-id="d858a-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d858a-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d858a-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d858a-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="d858a-186">CLSID</span></span><br/>                    | <span data-ttu-id="d858a-187">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d858a-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d858a-188">IID</span><span class="sxs-lookup"><span data-stu-id="d858a-188">IID</span></span><br/>                      | <span data-ttu-id="d858a-189">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="d858a-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d858a-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d858a-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d858a-191">**M**</span><span class="sxs-lookup"><span data-stu-id="d858a-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="d858a-192">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="d858a-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="d858a-193">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="d858a-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="d858a-194">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="d858a-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

