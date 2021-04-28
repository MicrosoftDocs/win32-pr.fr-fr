---
description: SWbemServices.Exeméthode cMethod-exécute une méthode exportée par un fournisseur de méthode.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cMethod (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103637"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="42b11-103">SWbemServices.Exeméthode cMethod</span><span class="sxs-lookup"><span data-stu-id="42b11-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="42b11-104">La méthode **ExecMethod** de l’objet [**SWbemServices**](swbemservices.md) exécute une méthode qui est exportée par un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="42b11-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="42b11-105">Cette méthode bloque pendant l’exécution de la méthode qui est transférée au fournisseur approprié.</span><span class="sxs-lookup"><span data-stu-id="42b11-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="42b11-106">Les informations et l’État sont ensuite renvoyés.</span><span class="sxs-lookup"><span data-stu-id="42b11-106">The information and status are then returned.</span></span> <span data-ttu-id="42b11-107">Au lieu de WMI, le fournisseur implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="42b11-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="42b11-108">Cette méthode est appelée en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="42b11-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="42b11-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="42b11-110">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42b11-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42b11-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="42b11-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42b11-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b11-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="42b11-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="42b11-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="42b11-114">Required.</span></span> <span data-ttu-id="42b11-115">Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée.</span><span class="sxs-lookup"><span data-stu-id="42b11-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="42b11-116">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b11-117">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="42b11-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="42b11-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="42b11-118">Required.</span></span> <span data-ttu-id="42b11-119">Nom de la méthode pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="42b11-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-120">*objWbemInParams* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="42b11-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42b11-121">Objet [**SWbemObject**](swbemobject.md) qui contient les paramètres d’entrée de la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="42b11-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="42b11-122">Par défaut, ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="42b11-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="42b11-123">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="42b11-124">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="42b11-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42b11-125">Réservé.</span><span class="sxs-lookup"><span data-stu-id="42b11-125">Reserved.</span></span> <span data-ttu-id="42b11-126">Cette valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="42b11-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-127">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="42b11-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42b11-128">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="42b11-128">Typically, this is undefined.</span></span> <span data-ttu-id="42b11-129">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="42b11-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="42b11-130">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="42b11-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b11-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="42b11-131">Return value</span></span>

<span data-ttu-id="42b11-132">Si la méthode réussit, un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="42b11-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="42b11-133">L’objet retourné contient les paramètres de sortie et la valeur de retour pour la méthode en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="42b11-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42b11-134">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="42b11-134">Error codes</span></span>

<span data-ttu-id="42b11-135">Une fois la méthode **ExecMethod** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="42b11-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="42b11-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="42b11-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="42b11-137">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="42b11-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="42b11-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="42b11-139">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="42b11-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="42b11-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="42b11-141">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="42b11-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="42b11-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="42b11-143">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="42b11-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-144">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="42b11-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="42b11-145">La méthode demandée n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="42b11-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="42b11-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="42b11-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="42b11-147">L’utilisateur actuel n’a pas été autorisé à exécuter la méthode.</span><span class="sxs-lookup"><span data-stu-id="42b11-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42b11-148">Notes </span><span class="sxs-lookup"><span data-stu-id="42b11-148">Remarks</span></span>

<span data-ttu-id="42b11-149">Utilisez **SWbemServices.ExecMethod** comme alternative à l’accès direct pour l’exécution d’une [*méthode de fournisseur*](gloss-p.md) dans les cas où il n’est pas possible d’exécuter une méthode directement.</span><span class="sxs-lookup"><span data-stu-id="42b11-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="42b11-150">La méthode **ExecMethod** vous permet d’obtenir des paramètres de sortie, si le fournisseur les fournit, à l’aide d’un langage de script qui ne prend pas en charge les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="42b11-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="42b11-151">Dans le cas contraire, les méthodes recommandées pour appeler une méthode consiste à utiliser l’accès direct.</span><span class="sxs-lookup"><span data-stu-id="42b11-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="42b11-152">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="42b11-153">Par exemple, l’exemple de code suivant qui appelle la méthode du fournisseur [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) dans le [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) utilise l’accès direct.</span><span class="sxs-lookup"><span data-stu-id="42b11-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="42b11-154">Cet exemple appelle **SWbemServices.ExecMethod** pour exécuter la méthode [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="42b11-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="42b11-155">Notez qu’un chemin d’accès à l’objet est requis, car **SWbemServices.ExecMethod** ne fonctionne pas déjà sur l’objet, contrairement à [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="42b11-156">La méthode **SWbemServices.ExecMethod** requiert un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="42b11-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="42b11-157">Si le script contient déjà un objet [**SWbemObject**](swbemobject.md) , utilisez la méthode [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) .</span><span class="sxs-lookup"><span data-stu-id="42b11-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="42b11-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="42b11-158">Examples</span></span>

<span data-ttu-id="42b11-159">L’exemple suivant illustre la méthode **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="42b11-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="42b11-160">Le script crée un [**objet \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) qui représente un processus qui exécute le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="42b11-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="42b11-161">Il illustre la configuration d’un objet [**Parameters**](swbemmethod-inparameters.md) et l’obtention des résultats d’un objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="42b11-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="42b11-162">Pour obtenir un script qui montre les mêmes opérations exécutées de façon asynchrone, consultez [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="42b11-163">Pour obtenir un exemple d’utilisation de l’accès direct, consultez [créer une méthode dans la classe \_ processus Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="42b11-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="42b11-164">Pour obtenir un exemple de la même opération à l’aide d’un [**SWbemObject**](swbemobject.md), consultez [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="42b11-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="42b11-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42b11-165">Requirements</span></span>



| <span data-ttu-id="42b11-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42b11-166">Requirement</span></span> | <span data-ttu-id="42b11-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="42b11-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42b11-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42b11-168">Minimum supported client</span></span><br/> | <span data-ttu-id="42b11-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42b11-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42b11-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42b11-170">Minimum supported server</span></span><br/> | <span data-ttu-id="42b11-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42b11-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42b11-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="42b11-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="42b11-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42b11-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42b11-174">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="42b11-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="42b11-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42b11-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42b11-176">DLL</span><span class="sxs-lookup"><span data-stu-id="42b11-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42b11-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42b11-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42b11-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="42b11-178">CLSID</span></span><br/>                    | <span data-ttu-id="42b11-179">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="42b11-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="42b11-180">IID</span><span class="sxs-lookup"><span data-stu-id="42b11-180">IID</span></span><br/>                      | <span data-ttu-id="42b11-181">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="42b11-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="42b11-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42b11-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b11-183">**M**</span><span class="sxs-lookup"><span data-stu-id="42b11-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="42b11-184">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="42b11-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="42b11-185">Appel d’une méthode de fournisseur</span><span class="sxs-lookup"><span data-stu-id="42b11-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="42b11-186">Manipulation des informations relatives aux classes et aux instances</span><span class="sxs-lookup"><span data-stu-id="42b11-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

