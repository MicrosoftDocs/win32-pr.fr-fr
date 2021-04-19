---
description: Le fait d’effectuer un appel asynchrone à une méthode WMI ou à une méthode de fournisseur permet à un script de continuer à s’exécuter pendant que les objets retournent à un objet SWbemSink et sont gérés par des méthodes telles que SWbemSink. OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Exécution d’un appel asynchrone avec VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529855"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="a510c-103">Exécution d’un appel asynchrone avec VBScript</span><span class="sxs-lookup"><span data-stu-id="a510c-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="a510c-104">Le fait d’effectuer un appel asynchrone à une [*méthode WMI*](gloss-w.md) ou à une [*méthode de fournisseur*](gloss-p.md) permet à un script de continuer à s’exécuter pendant que les objets retournent à un objet [**SWbemSink**](swbemsink.md) et sont gérés par des méthodes telles que [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md).</span><span class="sxs-lookup"><span data-stu-id="a510c-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="a510c-105">Toutefois, les appels asynchrones ne sont pas recommandés, car les données peuvent ne pas être retournées au même niveau de sécurité à mesure que l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="a510c-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="a510c-106">Lorsque vous utilisez des appels de récepteur asynchrones comme [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) pour récupérer des données retournées, vous pouvez définir la valeur de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="a510c-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="a510c-107">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**</span><span class="sxs-lookup"><span data-stu-id="a510c-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="a510c-108">La définition de cette valeur de Registre garantit l’authentification des objets de données renvoyés au récepteur.</span><span class="sxs-lookup"><span data-stu-id="a510c-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="a510c-109">Si **UnsecAppAccessControlDefault** est défini sur un (1), WMI effectue la vérification de l’accès des données renvoyées.</span><span class="sxs-lookup"><span data-stu-id="a510c-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="a510c-110">Les vérifications d’accès vérifient que les données proviennent de la source correcte.</span><span class="sxs-lookup"><span data-stu-id="a510c-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="a510c-111">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="a510c-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="a510c-112">Les méthodes asynchrones avec des noms qui se terminent par « Async \_ » retournent toujours immédiatement après leur appel afin qu’un programme puisse continuer à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a510c-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="a510c-113">Par exemple, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) est synchrone et bloque l’exécution jusqu’à ce que tous les objets soient retournés.</span><span class="sxs-lookup"><span data-stu-id="a510c-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="a510c-114">La méthode [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) est la version asynchrone qui ne se bloque pas.</span><span class="sxs-lookup"><span data-stu-id="a510c-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="a510c-115">Une façon plus sécurisée d’effectuer l’appel àSWbemServices.Exele non-blocage **cQuery** consiste à effectuer l’appel [*semisynchronously*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="a510c-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="a510c-116">Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md) et [exécution d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a510c-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="a510c-117">Le paramètre *IFlags* pour les appels asynchrones est toujours défini par défaut sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="a510c-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="a510c-118">Les méthodes asynchrones ne fournissent pas de collection [**SWbemObjectSet**](swbemobjectset.md) à la sous-routine sink.</span><span class="sxs-lookup"><span data-stu-id="a510c-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="a510c-119">Au lieu de cela, la sous-routine d’événement [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) de votre script ou application reçoit chaque objet tel qu’il est fourni.</span><span class="sxs-lookup"><span data-stu-id="a510c-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="a510c-120">Lorsque l’appel asynchrone d’origine est terminé, il appelle l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) du récepteur d’objets et exécute le code que vous placez pour traiter le résultat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="a510c-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="a510c-121">Une page de Active Server (ASP) en tant qu’hôte de script ne prend pas en charge un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a510c-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="a510c-122">La procédure suivante décrit comment effectuer un appel asynchrone à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="a510c-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="a510c-123">**Pour effectuer un appel asynchrone à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="a510c-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="a510c-124">Connectez-vous à WMI et récupérez un objet [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="a510c-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="a510c-125">Créez le récepteur d’objets à l’aide de [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ou (pour Windows Script Host 2,0 uniquement) la balise Object avec un attribut Events ayant la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="a510c-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="a510c-126">-ou-</span><span class="sxs-lookup"><span data-stu-id="a510c-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="a510c-127">Créez une sous-routine pour chaque événement qu’un événement asynchrone peut déclencher.</span><span class="sxs-lookup"><span data-stu-id="a510c-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="a510c-128">Ces événements sont définis en tant que méthodes sur [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="a510c-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="a510c-129">Par exemple, WMI effectue un rappel à [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) à mesure que chaque instance retourne.</span><span class="sxs-lookup"><span data-stu-id="a510c-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="a510c-130">Lorsque vous créez la sous-routine, placez le code dans la sous-routine pour gérer chaque événement lors de sa réception.</span><span class="sxs-lookup"><span data-stu-id="a510c-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="a510c-131">Examinez le paramètre *iHresult* retourné par l’événement [**OnCompleted**](swbemsink-oncompleted.md) pour déterminer si l’appel asynchrone a réussi ou non, ou si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a510c-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="a510c-132">En cas de réussite, la valeur passée dans le paramètre *iHresult* est égale à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="a510c-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="a510c-133">Toute autre valeur peut indiquer une erreur, et vous devez vérifier les valeurs dans l’objet d’erreur qui est retourné dans le paramètre *objErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="a510c-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="a510c-134">Effectuez un appel asynchrone et transmettez le nom de votre récepteur dans le paramètre *objWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="a510c-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="a510c-135">Effectuez un appel qui empêche le script de se terminer avant la réception de tous les événements.</span><span class="sxs-lookup"><span data-stu-id="a510c-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="a510c-136">Si votre script peut s’exécuter avec une interface d’écran, un moyen simple de le faire consiste à utiliser une commande Windows Script Host (WSH) `Echo` , qui est illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a510c-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="a510c-137">Lorsque vous exécutez ce script, vous pouvez voir que la première instance est retournée avant le message **d’attente d’instances** ou que vous pouvez la voir après.</span><span class="sxs-lookup"><span data-stu-id="a510c-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="a510c-138">Il s’agit de la nature du traitement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a510c-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="a510c-139">Si vous fermez la boîte de message en **attente d’instances** trop tôt, vous ne verrez peut-être pas toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="a510c-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="a510c-140">Si vous avez des résultats de plusieurs appels asynchrones différents retournant au même récepteur, stockez toutes les données de différenciation nécessaires dans le paramètre de contexte *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="a510c-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="a510c-141">Lorsque vous avez terminé avec le récepteur, annulez votre appel asynchrone à l’aide de la méthode [**Cancel**](swbemsink-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="a510c-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="a510c-142">La méthode [**Cancel**](swbemsink-cancel.md) indique à WSH d’annuler tous les appels asynchrones associés à un objet récepteur donné.</span><span class="sxs-lookup"><span data-stu-id="a510c-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="a510c-143">Ainsi, vous souhaiterez peut-être utiliser des récepteurs distincts pour les opérations asynchrones qui doivent être indépendantes.</span><span class="sxs-lookup"><span data-stu-id="a510c-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="a510c-144">Libérer l’objet récepteur en lui assignant l’objet récepteur `Nothing` .</span><span class="sxs-lookup"><span data-stu-id="a510c-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="a510c-145">L’exemple de code suivant montre une requête asynchrone pour toutes les instances [**du \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a510c-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="a510c-146">Pour obtenir une version semi-synchrone de la même méthode, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a510c-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="a510c-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a510c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a510c-148">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="a510c-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="a510c-149">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="a510c-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
