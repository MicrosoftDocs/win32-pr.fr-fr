---
description: WMI fournit des méthodes dans l’API COM et l’API de script pour obtenir des informations ou manipuler des objets dans un système d’entreprise.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Appel d’une méthode WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535685"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="51277-103">Appel d’une méthode WMI</span><span class="sxs-lookup"><span data-stu-id="51277-103">Calling a WMI Method</span></span>

<span data-ttu-id="51277-104">WMI fournit des méthodes dans l' [API com](com-api-for-wmi.md) et l' [API de script](scripting-api-for-wmi.md) pour obtenir des informations ou manipuler des objets dans un système d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="51277-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="51277-105">Par exemple, la méthode de script WMI [**SWbemServices.Exe**](swbemservices-execquery.md) des requêtes cQuery pour les données.</span><span class="sxs-lookup"><span data-stu-id="51277-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="51277-106">Les fournisseurs ont également des méthodes définies dans les classes qu’ils inscrivent.</span><span class="sxs-lookup"><span data-stu-id="51277-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="51277-107">Exemples : les [**méthodes \_ logiques Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) et [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) fournies par le [fournisseur Win32](/windows/desktop/CIMWin32Prov/win32-provider).</span><span class="sxs-lookup"><span data-stu-id="51277-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="51277-108">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="51277-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="51277-109">Comparaison des méthodes WMI et des méthodes de fournisseur</span><span class="sxs-lookup"><span data-stu-id="51277-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="51277-110">Modes d’appel de méthode dans WMI</span><span class="sxs-lookup"><span data-stu-id="51277-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="51277-111">Mode synchrone</span><span class="sxs-lookup"><span data-stu-id="51277-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="51277-112">Mode asynchrone</span><span class="sxs-lookup"><span data-stu-id="51277-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="51277-113">Mode semi-synchrone</span><span class="sxs-lookup"><span data-stu-id="51277-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="51277-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51277-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="51277-115">Comparaison des méthodes WMI et des méthodes de fournisseur</span><span class="sxs-lookup"><span data-stu-id="51277-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="51277-116">En utilisant des appels de [*méthode WMI*](gloss-w.md) combinés aux appels de [*méthode de fournisseur*](gloss-p.md) , vous pouvez récupérer et manipuler les informations relatives à votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="51277-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="51277-117">Pour plus d’informations, consultez [appel d’une méthode WMI](calling-a-wmi-method.md) et [appel d’une méthode de fournisseur](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="51277-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="51277-118">Les méthodes de l’objet de script WMI [**SWbemObject**](swbemobject.md) ont un état spécial, car elles peuvent s’appliquer à n’importe quelle classe de données WMI.</span><span class="sxs-lookup"><span data-stu-id="51277-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="51277-119">Pour plus d’informations, consultez [Scripting with SWbemObject](scripting-with-swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="51277-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="51277-120">L’exemple de code suivant appelle les méthodes WMI et Provider.</span><span class="sxs-lookup"><span data-stu-id="51277-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="51277-121">Les méthodes WMI et Provider suivantes se trouvent dans l' [API de script pour WMI](scripting-api-for-wmi.md):</span><span class="sxs-lookup"><span data-stu-id="51277-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="51277-122">**objWMIService.ExecQuery** appelle la méthode de script WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="51277-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="51277-123">**objService. StopService ()** appelle la méthode du fournisseur [ **Win32 \_ service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="51277-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="51277-124">Vous pouvez rechercher le code qui peut s’afficher dans « retour » dans la section codes de retour [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="51277-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="51277-125">Modes de Method-Calling dans WMI</span><span class="sxs-lookup"><span data-stu-id="51277-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="51277-126">Le mode d’appel semi-synchrone offre généralement le meilleur équilibre entre la sécurité et les performances.</span><span class="sxs-lookup"><span data-stu-id="51277-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="51277-127">Pour plus d’informations sur chacun des modes possibles, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="51277-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="51277-128">Synchrone</span><span class="sxs-lookup"><span data-stu-id="51277-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="51277-129">Asynchrone</span><span class="sxs-lookup"><span data-stu-id="51277-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="51277-130">Semi</span><span class="sxs-lookup"><span data-stu-id="51277-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="51277-131">Mode synchrone</span><span class="sxs-lookup"><span data-stu-id="51277-131">Synchronous Mode</span></span>

<span data-ttu-id="51277-132">Le mode synchrone se produit lorsque le programme ou les scripts s’interrompt jusqu’à ce que l’appel de méthode retourne un objet de collection [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="51277-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="51277-133">WMI génère cette collection en mémoire avant de retourner l’objet de collection au programme ou au script appelant.</span><span class="sxs-lookup"><span data-stu-id="51277-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="51277-134">Le mode synchrone peut avoir un effet néfaste sur les performances des programmes ou des scripts sur l’ordinateur qui exécute le programme ou le script.</span><span class="sxs-lookup"><span data-stu-id="51277-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="51277-135">Par exemple, la récupération synchrone de milliers d’événements à partir du journal des événements peut prendre beaucoup de temps et utiliser beaucoup de mémoire, car WMI crée un objet à partir de chaque événement, puis place ces objets dans une collection avant de passer la collection à la méthode.</span><span class="sxs-lookup"><span data-stu-id="51277-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="51277-136">Vous devez uniquement appeler les méthodes qui ne retournent pas de jeux de données de grande taille en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="51277-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="51277-137">Les méthodes [**SWbemServices**](swbemservices.md) suivantes peuvent être appelées en toute sécurité en mode synchrone :</span><span class="sxs-lookup"><span data-stu-id="51277-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="51277-138">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="51277-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="51277-139">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="51277-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="51277-140">**SWbemServices.**</span><span class="sxs-lookup"><span data-stu-id="51277-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="51277-141">Toutes les méthodes [**SWbemServices**](swbemservices.md) sans le mot « Async » dans le nom peuvent être appelées en mode synchrone en définissant la valeur **wbemFlagReturnWhenComplete** dans le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="51277-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="51277-142">Mode asynchrone</span><span class="sxs-lookup"><span data-stu-id="51277-142">Asynchronous Mode</span></span>

<span data-ttu-id="51277-143">Le mode asynchrone se produit lorsque le programme ou le script continue à s’exécuter après l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="51277-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="51277-144">WMI retourne tous les objets de la méthode à un objet [**SWbemSink**](swbemsink.md) lors de la création de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="51277-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="51277-145">Le programme ou le script appelant doit avoir un objet **SWbemSink** et un gestionnaire d’événements [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) pour traiter les objets retournés.</span><span class="sxs-lookup"><span data-stu-id="51277-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="51277-146">Pour plus d’informations sur la création d’un gestionnaire d’événements pour le mode asynchrone, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="51277-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="51277-147">Bien que ce mode ne présente pas les performances et les ressources du mode synchrone, le mode asynchrone peut créer des risques sérieux pour la sécurité, car les résultats stockés dans l’objet [**SWbemSink**](swbemsink.md) peuvent ne pas provenir du programme ou du script appelant.</span><span class="sxs-lookup"><span data-stu-id="51277-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="51277-148">WMI réduit le niveau d’authentification sur l’objet **SWbemSink** jusqu’à ce que la méthode aboutisse.</span><span class="sxs-lookup"><span data-stu-id="51277-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="51277-149">Pour plus d’informations sur la façon de réduire ces risques de sécurité, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="51277-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="51277-150">Les méthodes ajoutées au mot Async sont des méthodes pour le mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="51277-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="51277-151">Les méthodes suivantes sont des appels asynchrones :</span><span class="sxs-lookup"><span data-stu-id="51277-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="51277-152">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="51277-153">**SWbemServices. DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="51277-154">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="51277-155">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="51277-156">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="51277-157">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="51277-158">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="51277-159">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="51277-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="51277-160">Pour plus d’informations sur le mode asynchrone, consultez :</span><span class="sxs-lookup"><span data-stu-id="51277-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="51277-161">Exécution d’un appel asynchrone avec C++</span><span class="sxs-lookup"><span data-stu-id="51277-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="51277-162">Exécution d’un appel asynchrone avec VBScript</span><span class="sxs-lookup"><span data-stu-id="51277-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="51277-163">Mode semi-synchrone</span><span class="sxs-lookup"><span data-stu-id="51277-163">Semisynchronous Mode</span></span>

<span data-ttu-id="51277-164">Le mode semi-synchrone est semblable au mode asynchrone en ce que le programme ou le script continue à s’exécuter après l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="51277-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="51277-165">En mode semi-synchrone, WMI récupère les objets en arrière-plan au fur et à mesure que votre script ou votre programme continue de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="51277-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="51277-166">WMI retourne chaque objet retourné à la méthode appelante juste après la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="51277-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="51277-167">Étant donné que WMI gère l’objet, le mode semi-synchrone est plus sécurisé que le mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="51277-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="51277-168">Toutefois, si vous utilisez le mode semi-synchrone avec plus de 1 000 instances, la récupération d’instance peut monopoliser les ressources disponibles, ce qui peut dégrader les performances du programme ou du script et de l’ordinateur à l’aide du programme ou du script.</span><span class="sxs-lookup"><span data-stu-id="51277-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="51277-169">Chaque objet utilise les ressources nécessaires jusqu’à ce que la mémoire soit libérée.</span><span class="sxs-lookup"><span data-stu-id="51277-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="51277-170">Pour contourner cette condition, vous pouvez appeler la méthode avec le paramètre *IFlags* défini avec les indicateurs **wbemFlagForwardOnly** et **wbemFlagReturnImmediately** pour indiquer à WMI de retourner une [**SWbemObjectSet**](swbemobjectset.md)avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="51277-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="51277-171">Un objet **SWbemObjectSet** avant uniquement élimine le problème de performance causé par un jeu de données volumineux en libérant la mémoire après l’énumération de l’objet.</span><span class="sxs-lookup"><span data-stu-id="51277-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="51277-172">Toute méthode [**SWbemServices**](swbemservices.md) qui ne peut pas être appelée en mode synchrone ou asynchrone est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="51277-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="51277-173">Les méthodes suivantes sont appelées en mode semi-synchrone :</span><span class="sxs-lookup"><span data-stu-id="51277-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="51277-174">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="51277-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="51277-175">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="51277-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="51277-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="51277-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="51277-177">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="51277-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="51277-178">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="51277-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="51277-179">**SWbemServices.**</span><span class="sxs-lookup"><span data-stu-id="51277-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="51277-180">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="51277-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="51277-181">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="51277-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="51277-182">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="51277-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="51277-183">**SWbemServices. put**</span><span class="sxs-lookup"><span data-stu-id="51277-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="51277-184">Pour plus d’informations sur le mode semi-synchrone, consultez [création d’un appel semi-synchrone avec C++](making-a-semisynchronous-call-with-c--.md) et [exécution d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="51277-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51277-185">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51277-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51277-186">Amélioration des performances d’énumération</span><span class="sxs-lookup"><span data-stu-id="51277-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="51277-187">Écriture de scripts avec SWbemObject</span><span class="sxs-lookup"><span data-stu-id="51277-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="51277-188">**WbemFlagEnum**</span><span class="sxs-lookup"><span data-stu-id="51277-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
