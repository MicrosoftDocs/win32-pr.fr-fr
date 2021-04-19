---
description: Récupère un objet, qui est soit une définition de classe, soit une instance, en fonction du chemin d’accès de l’objet.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: SWbemServices. obten, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8998a1ca04206362fcc0e7405fccf8c923d74d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518725"
---
# <a name="swbemservicesget-method"></a><span data-ttu-id="eb011-103">SWbemServices. obten, méthode</span><span class="sxs-lookup"><span data-stu-id="eb011-103">SWbemServices.Get method</span></span>

<span data-ttu-id="eb011-104">La **méthode d’extraction de** l’objet [**SWbemServices**](swbemservices.md) récupère un objet, qui est soit une définition de classe, soit une instance, en fonction du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eb011-104">The **Get** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is either a class definition or an instance, based on the object path.</span></span> <span data-ttu-id="eb011-105">Cette méthode récupère uniquement les objets de l’espace de noms associé à l’objet **SWbemServices** actif.</span><span class="sxs-lookup"><span data-stu-id="eb011-105">This method retrieves only objects from the namespace that is associated with the current **SWbemServices** object.</span></span>

<span data-ttu-id="eb011-106">La méthode est appelée en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="eb011-106">The method is called in the synchronous mode.</span></span> <span data-ttu-id="eb011-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb011-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="eb011-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb011-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb011-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb011-109">Syntax</span></span>


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb011-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb011-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb011-111">*strObjectPath* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb011-111">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb011-112">Chaîne qui contient le chemin d’accès de l’objet à récupérer.</span><span class="sxs-lookup"><span data-stu-id="eb011-112">String that contains the object path of the object to retrieve.</span></span> <span data-ttu-id="eb011-113">Si cette valeur est vide, l’objet vide retourné peut devenir une nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="eb011-113">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="eb011-114">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="eb011-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb011-115">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb011-115">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb011-116">Entier qui détermine le comportement de la requête.</span><span class="sxs-lookup"><span data-stu-id="eb011-116">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="eb011-117">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb011-117">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="eb011-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="eb011-118"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="eb011-119">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="eb011-119">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="eb011-120">Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="eb011-120">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb011-121">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb011-121">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb011-122">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="eb011-122">Typically, this is undefined.</span></span> <span data-ttu-id="eb011-123">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="eb011-123">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eb011-124">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="eb011-124">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb011-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb011-125">Return value</span></span>

<span data-ttu-id="eb011-126">En cas de réussite, cette méthode retourne un objet [**SWbemObject**](swbemobject.md) qui représente l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="eb011-126">If successful, this method returns an [**SWbemObject**](swbemobject.md) object that represents the requested object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb011-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eb011-127">Error codes</span></span>

<span data-ttu-id="eb011-128">À la fin de la méthode d' **extraction** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="eb011-128">Upon the completion of the **Get** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eb011-129">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="eb011-129">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eb011-130">L’utilisateur actuel n’a pas l’autorisation d’accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="eb011-130">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="eb011-131">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eb011-131">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb011-132">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eb011-132">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eb011-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="eb011-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eb011-134">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="eb011-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb011-135">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="eb011-135">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="eb011-136">Le chemin d’accès spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="eb011-136">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb011-137">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="eb011-137">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="eb011-138">L’objet demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="eb011-138">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="eb011-139">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eb011-139">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb011-140">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb011-140">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb011-141">Notes</span><span class="sxs-lookup"><span data-stu-id="eb011-141">Remarks</span></span>

<span data-ttu-id="eb011-142">Contrairement aux méthodes [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) et [**InstancesOf**](swbemservices-instancesof.md) , la méthode obtenir retourne toujours un [**SWbemObject**](swbemobject.md) représentant une instance spécifique d’une ressource managée par WMI.</span><span class="sxs-lookup"><span data-stu-id="eb011-142">Unlike the [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) and [**InstancesOf**](swbemservices-instancesof.md) methods, the Get method always returns an [**SWbemObject**](swbemobject.md) representing a specific instance of a WMI-managed resource.</span></span> <span data-ttu-id="eb011-143">Pour obtenir une instance spécifique d’une ressource managée WMI à l’aide de la méthode obtenir, vous devez indiquer à l’instance de récupérer l’instance en passant la méthode au chemin d’accès de l’objet, comme indiqué dans le script suivant.</span><span class="sxs-lookup"><span data-stu-id="eb011-143">To obtain a specific instance of a WMI-managed resource using the Get method, you must tell Get the instance to retrieve by passing the method the object path, as shown in the following script.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



<span data-ttu-id="eb011-144">Vous pouvez utiliser cette méthode pour obtenir des objets [*Singleton*](gloss-s.md) , tels que [**\_ \_ CIMOMIdentification**](--cimomidentification.md), qui contient des informations de version sur l’installation WMI en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb011-144">You can use this method to obtain [*singleton*](gloss-s.md) objects, such as [**\_\_CIMOMIdentification**](--cimomidentification.md), which contains version information about the WMI installation that is running.</span></span>

<span data-ttu-id="eb011-145">Vous pouvez examiner le référentiel à l’aide d’un outil d’affichage tel que [CIM Studio](further-information.md) pour vérifier que la nouvelle classe et l’instance s’affichent.</span><span class="sxs-lookup"><span data-stu-id="eb011-145">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="eb011-146">Pour obtenir un exemple de suppression d’une classe et d’une instance du référentiel, consultez [**SWbemServices. Delete**](swbemservices-delete.md) ou [**SWbemObject. \_ Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="eb011-146">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb011-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb011-147">Requirements</span></span>



| <span data-ttu-id="eb011-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb011-148">Requirement</span></span> | <span data-ttu-id="eb011-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb011-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb011-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb011-150">Minimum supported client</span></span><br/> | <span data-ttu-id="eb011-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb011-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb011-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb011-152">Minimum supported server</span></span><br/> | <span data-ttu-id="eb011-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb011-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb011-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb011-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb011-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb011-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb011-156">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eb011-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb011-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb011-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb011-158">DLL</span><span class="sxs-lookup"><span data-stu-id="eb011-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb011-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb011-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb011-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb011-160">CLSID</span></span><br/>                    | <span data-ttu-id="eb011-161">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="eb011-161">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="eb011-162">IID</span><span class="sxs-lookup"><span data-stu-id="eb011-162">IID</span></span><br/>                      | <span data-ttu-id="eb011-163">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="eb011-163">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="eb011-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb011-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb011-165">**M**</span><span class="sxs-lookup"><span data-stu-id="eb011-165">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="eb011-166">**M**</span><span class="sxs-lookup"><span data-stu-id="eb011-166">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




