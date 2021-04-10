---
description: La \_ méthode ExecMethod de l’objet SWbemObject exécute une méthode exportée par un fournisseur de méthode.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: SWbemObject.Exeméthode cMethod_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114867"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="a4d59-103">SWbemObject.Exe\_ méthode cMethod</span><span class="sxs-lookup"><span data-stu-id="a4d59-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="a4d59-104">La **méthode \_ ExecMethod** de l’objet [**SWbemObject**](swbemobject.md) exécute une méthode exportée par un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="a4d59-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="a4d59-105">Cette méthode s’interrompt pendant l’exécution de la méthode qui est transférée au fournisseur approprié.</span><span class="sxs-lookup"><span data-stu-id="a4d59-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="a4d59-106">Les informations et l’État sont ensuite renvoyés.</span><span class="sxs-lookup"><span data-stu-id="a4d59-106">The information and status are then returned.</span></span> <span data-ttu-id="a4d59-107">Le fournisseur plutôt que WMI implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="a4d59-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="a4d59-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a4d59-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d59-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4d59-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a4d59-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4d59-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d59-111">*strMethodName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4d59-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4d59-112">Required.</span></span> <span data-ttu-id="a4d59-113">Nom de la méthode pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="a4d59-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-114">*objwbemInParams* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a4d59-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-115">Il s’agit d’un objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a4d59-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="a4d59-116">Par défaut, ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="a4d59-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="a4d59-117">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a4d59-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-118">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a4d59-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-119">Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a4d59-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-120">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a4d59-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-121">En règle générale, il n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="a4d59-121">Typically, it is undefined.</span></span> <span data-ttu-id="a4d59-122">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="a4d59-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a4d59-123">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="a4d59-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d59-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4d59-124">Return value</span></span>

<span data-ttu-id="a4d59-125">Si cette méthode réussit, un objet [**SWbemObject**](swbemobject.md) retourne.</span><span class="sxs-lookup"><span data-stu-id="a4d59-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="a4d59-126">L’objet retourné contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a4d59-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a4d59-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a4d59-127">Error codes</span></span>

<span data-ttu-id="a4d59-128">Une fois la méthode **ExecMethod \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a4d59-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a4d59-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a4d59-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-130">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a4d59-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-131">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="a4d59-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-132">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a4d59-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a4d59-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-134">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a4d59-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-135">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a4d59-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-136">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a4d59-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-137">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="a4d59-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-138">La méthode demandée n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a4d59-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="a4d59-139">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="a4d59-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a4d59-140">L’utilisateur actuel n’a pas été autorisé à exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="a4d59-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4d59-141">Notes</span><span class="sxs-lookup"><span data-stu-id="a4d59-141">Remarks</span></span>

<span data-ttu-id="a4d59-142">Cette méthode est similaire à [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), mais elle fonctionne directement sur l’objet dont la méthode doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="a4d59-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="a4d59-143">Par exemple, l’exemple de code suivant appelle la méthode du fournisseur [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) dans le [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) et utilise l' [accès direct](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="a4d59-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="a4d59-144">Cette version appelle **SWbemObject.ExecMethod \_** pour exécuter la méthode [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="a4d59-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="a4d59-145">Utilisez **SWbemObject.ExecMethod \_** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) dans les cas où il n’est pas possible d’exécuter une méthode directement.</span><span class="sxs-lookup"><span data-stu-id="a4d59-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="a4d59-146">Par exemple, vous pouvez utiliser **SWbemObject.ExecMethod \_** avec un langage de script qui ne prend pas en charge les paramètres de sortie si votre méthode a des paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="a4d59-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="a4d59-147">Dans le cas contraire, les méthodes recommandées pour appeler une méthode consiste à utiliser l’accès direct.</span><span class="sxs-lookup"><span data-stu-id="a4d59-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="a4d59-148">La méthode **SWbemObject.Exe\_ cMethod** suppose que l’objet représenté par [**SWbemObject**](swbemobject.md) contient la méthode à exécuter.</span><span class="sxs-lookup"><span data-stu-id="a4d59-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="a4d59-149">En revanche, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requiert un chemin d’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="a4d59-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="a4d59-150">Utilisez **SWbemObject.ExecMethod \_** si vous avez déjà obtenu l’objet dont vous souhaitez exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="a4d59-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="a4d59-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="a4d59-151">Examples</span></span>

<span data-ttu-id="a4d59-152">L’exemple suivant illustre la méthode [**ExecMethod**](swbemservices-execmethod.md) . Le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) représentant un processus qui exécute le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="a4d59-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="a4d59-153">Pour plus d’informations sur un script illustrant les mêmes opérations exécutées de façon asynchrone, consultez [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="a4d59-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="a4d59-154">Pour obtenir un exemple d’utilisation de l’accès direct, consultez [**créer une méthode dans la classe \_ processus Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="a4d59-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="a4d59-155">Pour obtenir un exemple de la même opération à l’aide d’un objet [**SWbemServices**](swbemservices.md) , consultez **SWbemServices.ExecMethod**.</span><span class="sxs-lookup"><span data-stu-id="a4d59-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="a4d59-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4d59-156">Requirements</span></span>



| <span data-ttu-id="a4d59-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4d59-157">Requirement</span></span> | <span data-ttu-id="a4d59-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4d59-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d59-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4d59-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d59-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4d59-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4d59-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4d59-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d59-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4d59-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4d59-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4d59-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4d59-164"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4d59-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4d59-165">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a4d59-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4d59-166"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4d59-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4d59-167">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d59-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d59-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d59-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4d59-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="a4d59-169">CLSID</span></span><br/>                    | <span data-ttu-id="a4d59-170">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="a4d59-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="a4d59-171">IID</span><span class="sxs-lookup"><span data-stu-id="a4d59-171">IID</span></span><br/>                      | <span data-ttu-id="a4d59-172">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="a4d59-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="a4d59-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4d59-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d59-174">**M**</span><span class="sxs-lookup"><span data-stu-id="a4d59-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="a4d59-175">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="a4d59-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="a4d59-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="a4d59-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

