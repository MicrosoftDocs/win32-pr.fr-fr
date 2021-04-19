---
description: Comme avec toutes les applications, WMI reçoit les codes d’erreur du système d’exploitation Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Récupération d’un code d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516988"
---
# <a name="retrieving-an-error-code"></a><span data-ttu-id="1980d-103">Récupération d’un code d’erreur</span><span class="sxs-lookup"><span data-stu-id="1980d-103">Retrieving an Error Code</span></span>

<span data-ttu-id="1980d-104">Comme avec toutes les applications, WMI reçoit les codes d’erreur du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="1980d-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="1980d-105">Lorsque vous recevez un code d’erreur, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1980d-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="1980d-106">Examinez le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="1980d-106">Look at the event log.</span></span>

    <span data-ttu-id="1980d-107">WMI envoie des messages d’erreur au service journal des événements qui vérifie les journaux des événements pour déterminer la cause d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="1980d-108">Vous pouvez utiliser les classes prises en charge par le fournisseur de [journaux des événements](/previous-versions/windows/desktop/eventlogprov/event-log-provider) pour accéder aux journaux des événements par programmation.</span><span class="sxs-lookup"><span data-stu-id="1980d-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="1980d-109">Récupérez le code d’erreur normalement.</span><span class="sxs-lookup"><span data-stu-id="1980d-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="1980d-110">WMI prend en charge les techniques standard pour récupérer les codes d’erreur, qui sont des codes d’erreur COM pour C++, et des objets d’erreur natifs, tels que [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), ou [**SWbemLastError**](swbemlasterror.md) si le fournisseur fournit des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="1980d-111">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="1980d-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="1980d-112">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="1980d-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="1980d-113">Gestion d’une erreur avec VBScript</span><span class="sxs-lookup"><span data-stu-id="1980d-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="1980d-114">Gestion d’une erreur à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="1980d-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="1980d-115">Gestion d’une erreur avec VBScript</span><span class="sxs-lookup"><span data-stu-id="1980d-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="1980d-116">Si un appel à WMI par le biais de l’API de script pour WMI provoque une erreur, vous disposez des options suivantes pour accéder aux informations d’erreur :</span><span class="sxs-lookup"><span data-stu-id="1980d-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="1980d-117">Utilisez des mécanismes d’erreur natifs du langage de script. par exemple, dans VBScript, utilisez [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) pour prendre en charge la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1980d-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="1980d-118">Créez un objet [**SWbemLastError**](swbemlasterror.md) pour recevoir un rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="1980d-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="1980d-119">Le script suivant illustre l’utilisation de l' [objet Native Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1980d-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="1980d-120">Lorsqu’une valeur incorrecte pour le handle de processus est spécifiée, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="1980d-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="1980d-121">La propriété **Description** de l' [objet Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) est vide lors de la connexion à WMI par le biais du moniker « winmgmts : ».</span><span class="sxs-lookup"><span data-stu-id="1980d-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="1980d-122">Toutefois, si vous vous connectez à l’aide de [**SWbemLocator**](swbemlocator.md), la description est disponible.</span><span class="sxs-lookup"><span data-stu-id="1980d-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="1980d-123">Le tableau suivant répertorie les propriétés de l' [objet Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1980d-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="1980d-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="1980d-124">Property</span></span>                   | <span data-ttu-id="1980d-125">Contient</span><span class="sxs-lookup"><span data-stu-id="1980d-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="1980d-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="1980d-126">**Description**</span></span><br/> | <span data-ttu-id="1980d-127">Description localisée et explicite de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="1980d-128">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1980d-128">**Number**</span></span><br/>      | <span data-ttu-id="1980d-129">**HRESULT** retourné par l’API de script pour WMI.</span><span class="sxs-lookup"><span data-stu-id="1980d-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="1980d-130">**Source**</span><span class="sxs-lookup"><span data-stu-id="1980d-130">**Source**</span></span><br/>      | <span data-ttu-id="1980d-131">Identifie l’objet qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="1980d-132">Le script suivant illustre l’utilisation d’un objet [**SWbemLastError**](swbemlasterror.md) pour obtenir des informations détaillées sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="1980d-133">Notez que tous les fournisseurs ne fournissent pas d’informations à **SWbemLastError**.</span><span class="sxs-lookup"><span data-stu-id="1980d-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="1980d-134">Pour plus d’informations sur les codes d’erreur dans le script, consultez [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1980d-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="1980d-135">Gestion d’une erreur à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="1980d-135">Handling an Error Using C++</span></span>

<span data-ttu-id="1980d-136">Une application cliente WMI peut recevoir des erreurs spécifiques à COM ou à WMI.</span><span class="sxs-lookup"><span data-stu-id="1980d-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="1980d-137">Les erreurs COM sont conformes à la structure des codes d’erreur COM.</span><span class="sxs-lookup"><span data-stu-id="1980d-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="1980d-138">Toutes les interfaces WMI peuvent retourner une erreur spécifique à COM, à l’exception des interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)et [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="1980d-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="1980d-139">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="1980d-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="1980d-140">Les pages de référence des interfaces WMI répertorient les codes d’erreur WMI appropriés dans la section Codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="1980d-141">Une application cliente doit suivre les normes COM pour vérifier l’État et les codes de retour d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="1980d-142">La principale différence que vous devez choisir est de savoir si vous souhaitez récupérer le code d’erreur à partir d’un appel synchrone, semi-synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1980d-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="1980d-143">**Pour accéder aux messages d’erreur synchrones et semi-synchrones à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="1980d-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="1980d-144">Récupérez les informations d’erreur avec un appel à la fonction com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="1980d-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="1980d-145">Veillez à appeler [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immédiatement après qu’une méthode d’interface indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="1980d-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="1980d-146">Cela comprend l’une des méthodes [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) que vous appelez lors du traitement d’un processus semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="1980d-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="1980d-147">Examinez l’objet d’erreur COM retourné avec un appel à la méthode [**IErrorInterface :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="1980d-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="1980d-148">Veillez à spécifier IID \_ WbemClassObject pour le paramètre *riid* dans l’appel [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="1980d-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="1980d-149">La méthode **QueryInterface** retourne une instance d’une classe WMI, généralement [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1980d-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="1980d-150">WMI ne remet pas l’objet d’erreur via [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) pour un appel asynchrone, car il n’existe aucun moyen de savoir quand, ou sur quel thread l’appel asynchrone s’est produit.</span><span class="sxs-lookup"><span data-stu-id="1980d-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="1980d-151">Par conséquent, votre code peut uniquement gérer des erreurs spécifiques ou passer l’échec de l’appel par le biais de COM.</span><span class="sxs-lookup"><span data-stu-id="1980d-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="1980d-152">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1980d-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="1980d-153">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1980d-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="1980d-154">**Pour accéder aux messages d’erreur asynchrones à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="1980d-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="1980d-155">Récupérez l’objet d’erreur COM à partir de votre implémentation de [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="1980d-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="1980d-156">Le pseudo-code suivant illustre une implémentation de gestion des erreurs typique pour une application cliente.</span><span class="sxs-lookup"><span data-stu-id="1980d-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

