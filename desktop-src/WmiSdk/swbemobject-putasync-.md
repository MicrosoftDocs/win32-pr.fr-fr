---
description: La \_ méthode PutAsync de SWbemObject crée ou met à jour de manière asynchrone une instance ou un objet de classe à Windows Management Instrumentation (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Méthode SWbemObject.PutAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210552"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="935ed-103">SWbemObject. PutAsync, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="935ed-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="935ed-104">La **méthode \_ PutAsync** de [**SWbemObject**](swbemobject.md) crée ou met à jour de manière asynchrone une instance ou un objet de classe à Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="935ed-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="935ed-105">Vous pouvez utiliser cette méthode après avoir modifié des propriétés ou des méthodes dans **SWbemObject**, et vos modifications sont écrites dans WMI.</span><span class="sxs-lookup"><span data-stu-id="935ed-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="935ed-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="935ed-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="935ed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="935ed-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="935ed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="935ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="935ed-109">*objWbemSink* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="935ed-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935ed-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="935ed-110">Required.</span></span> <span data-ttu-id="935ed-111">Récepteur d’objets qui reçoit de façon asynchrone le résultat de l’opération **put** .</span><span class="sxs-lookup"><span data-stu-id="935ed-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-112">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="935ed-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="935ed-113">Détermine si l’appel crée ou met à jour la classe ou l’instance et si l’appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="935ed-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="935ed-114">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="935ed-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="935ed-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="935ed-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-116">Permet à une classe d’être mise à jour s’il n’y a pas de classes dérivées et qu’il n’existe aucune instance pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="935ed-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="935ed-117">Il autorise également les mises à jour dans tous les cas si la modification concerne uniquement des qualificateurs peu importants (par exemple, le qualificateur de **Description** ).</span><span class="sxs-lookup"><span data-stu-id="935ed-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="935ed-118">Il s’agit du comportement par défaut pour cet appel et est utilisé pour la compatibilité avec les versions précédentes de WMI.</span><span class="sxs-lookup"><span data-stu-id="935ed-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="935ed-119">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="935ed-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="935ed-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="935ed-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-121">Autorise les mises à jour des classes, même s’il existe des classes enfants, si la modification ne provoque pas de conflits avec les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="935ed-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="935ed-122">Vous pouvez utiliser cet indicateur lors de l’ajout d’une nouvelle propriété à une classe de base qui n’a pas été mentionnée précédemment dans une des classes enfants.</span><span class="sxs-lookup"><span data-stu-id="935ed-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="935ed-123">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="935ed-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="935ed-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="935ed-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-125">Force les mises à jour des classes lorsque des classes enfants sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="935ed-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="935ed-126">Par exemple, cet indicateur force une mise à jour si un qualificateur de classe a été défini dans une classe enfant, et si la classe de base tente d’ajouter le même qualificateur en conflit avec l’identificateur existant.</span><span class="sxs-lookup"><span data-stu-id="935ed-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="935ed-127">En mode de forçage, ce conflit est résolu en supprimant le qualificateur en conflit dans la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="935ed-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="935ed-128">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="935ed-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="935ed-129">L’utilisation du mode force pour mettre à jour une classe statique entraîne la suppression de toutes les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="935ed-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="935ed-130">Une mise à jour forcée sur une classe de fournisseur ne supprime pas les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="935ed-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="935ed-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="935ed-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-132">Provoque la création de la classe ou de l’instance si elle n’existe pas ou est remplacée si elle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="935ed-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="935ed-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="935ed-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-134">Utilisé pour la création uniquement.</span><span class="sxs-lookup"><span data-stu-id="935ed-134">Used for creation only.</span></span> <span data-ttu-id="935ed-135">L’appel échoue si la classe ou l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="935ed-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="935ed-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="935ed-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-137">Provoque la mise à jour de cet appel.</span><span class="sxs-lookup"><span data-stu-id="935ed-137">Causes this call to update.</span></span> <span data-ttu-id="935ed-138">La classe ou l’instance doit exister pour que l’appel réussisse.</span><span class="sxs-lookup"><span data-stu-id="935ed-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="935ed-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="935ed-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-140">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="935ed-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="935ed-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="935ed-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-142">Provoque le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="935ed-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="935ed-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="935ed-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-144">Fait en sorte que les appels asynchrones envoient des mises à jour d’État au gestionnaire d’événements [**SWbemSink. OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="935ed-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="935ed-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="935ed-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-146">Empêche les appels asynchrones d’envoyer des mises à jour d’État au gestionnaire d’événements [**OnProgress**](swbemsink-onprogress.md) pour le récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="935ed-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="935ed-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="935ed-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="935ed-148">Permet à WMI d’écrire des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="935ed-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="935ed-149">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="935ed-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="935ed-150">*objWbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="935ed-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="935ed-151">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="935ed-151">Typically, this is undefined.</span></span> <span data-ttu-id="935ed-152">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="935ed-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="935ed-153">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="935ed-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-154">*objWbemAsyncContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="935ed-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="935ed-155">Il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui retourne au récepteur d’objets pour identifier la source de l’appel asynchrone d’origine.</span><span class="sxs-lookup"><span data-stu-id="935ed-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="935ed-156">Utilisez ce paramètre si vous effectuez plusieurs appels asynchrones à l’aide du même récepteur d’objets.</span><span class="sxs-lookup"><span data-stu-id="935ed-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="935ed-157">Pour utiliser ce paramètre, créez un objet **SWbemNamedValueSet** et utilisez la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) pour ajouter une valeur qui identifie l’appel asynchrone que vous effectuez.</span><span class="sxs-lookup"><span data-stu-id="935ed-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="935ed-158">Cet objet **SWbemNamedValueSet** est retourné au récepteur d’objets et la source de l’appel peut être extraite à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="935ed-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="935ed-159">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="935ed-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="935ed-160">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="935ed-160">Return value</span></span>

<span data-ttu-id="935ed-161">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="935ed-161">This method does not return a value.</span></span> <span data-ttu-id="935ed-162">Si l’appel réussit, l’événement [**OnObjectPut**](swbemsink-onobjectput.md) du récepteur d’objets fourni reçoit un objet [**SWbemObjectPath**](swbemobjectpath.md) , contenant le chemin d’accès à l’objet de l’instance ou de la classe qui est correctement validée dans WMI.</span><span class="sxs-lookup"><span data-stu-id="935ed-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="935ed-163">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="935ed-163">Error codes</span></span>

<span data-ttu-id="935ed-164">À la fin de la **méthode \_ PutAsync** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="935ed-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="935ed-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="935ed-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-166">L’utilisateur actuel n’est pas autorisé à mettre à jour une instance de la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="935ed-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-167">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="935ed-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-168">L’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.</span><span class="sxs-lookup"><span data-stu-id="935ed-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-169">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="935ed-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-170">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="935ed-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-171">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="935ed-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-172">La valeur **Nothing** a été spécifiée pour une propriété qui ne peut pas être **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="935ed-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="935ed-173">Un exemple d’une telle propriété est une propriété qui est marquée par un qualificateur de **clé**, **indexée** ou **not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="935ed-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-174">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="935ed-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-175">L'instance spécifiée n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="935ed-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-176">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="935ed-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-177">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="935ed-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="935ed-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-179">L’indicateur **wbemChangeFlagUpdateOnly** a été spécifié, mais l’instance ou la classe n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="935ed-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-180">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="935ed-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-181">Les propriétés requises pour les classes n’ont pas toutes été définies.</span><span class="sxs-lookup"><span data-stu-id="935ed-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="935ed-182">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="935ed-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="935ed-183">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="935ed-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="935ed-184">Notes</span><span class="sxs-lookup"><span data-stu-id="935ed-184">Remarks</span></span>

<span data-ttu-id="935ed-185">Cet appel est retourné immédiatement, et le résultat de l’opération **put** est retourné à l’appelant via des rappels remis au récepteur spécifié dans *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="935ed-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="935ed-186">Implémentez *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="935ed-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="935ed-187">Méthode [**OnObjectPut**](swbemsink-onobjectput.md) pour obtenir le chemin d’accès de l’objet de l’instance ou de la classe écrite dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="935ed-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="935ed-188">Pour plus d’informations sur les méthodes de récepteur, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="935ed-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="935ed-189">Un rappel asynchrone permet à un utilisateur non authentifié de fournir des données au récepteur.</span><span class="sxs-lookup"><span data-stu-id="935ed-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="935ed-190">Cela pose des risques de sécurité pour vos scripts et vos applications.</span><span class="sxs-lookup"><span data-stu-id="935ed-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="935ed-191">Pour éliminer les risques, utilisez une communication semi-synchrone ou synchrone.</span><span class="sxs-lookup"><span data-stu-id="935ed-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="935ed-192">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="935ed-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="935ed-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="935ed-193">Requirements</span></span>



| <span data-ttu-id="935ed-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="935ed-194">Requirement</span></span> | <span data-ttu-id="935ed-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="935ed-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="935ed-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="935ed-196">Minimum supported client</span></span><br/> | <span data-ttu-id="935ed-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="935ed-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="935ed-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="935ed-198">Minimum supported server</span></span><br/> | <span data-ttu-id="935ed-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="935ed-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="935ed-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="935ed-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="935ed-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="935ed-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="935ed-202">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="935ed-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="935ed-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="935ed-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="935ed-204">DLL</span><span class="sxs-lookup"><span data-stu-id="935ed-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="935ed-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935ed-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="935ed-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="935ed-206">CLSID</span></span><br/>                    | <span data-ttu-id="935ed-207">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="935ed-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="935ed-208">IID</span><span class="sxs-lookup"><span data-stu-id="935ed-208">IID</span></span><br/>                      | <span data-ttu-id="935ed-209">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="935ed-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="935ed-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="935ed-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935ed-211">**M**</span><span class="sxs-lookup"><span data-stu-id="935ed-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="935ed-212">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="935ed-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="935ed-213">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="935ed-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="935ed-214">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="935ed-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

