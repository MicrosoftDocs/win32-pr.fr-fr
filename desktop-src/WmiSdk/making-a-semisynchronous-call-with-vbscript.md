---
description: Fournit des fonctionnalités d’accès semi-synchrone et un exemple de code pour effectuer un appel de méthode semi-synchrone.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Exécution d’un appel semi-synchrone avec VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527671"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="f28eb-103">Exécution d’un appel semi-synchrone avec VBScript</span><span class="sxs-lookup"><span data-stu-id="f28eb-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="f28eb-104">Certaines méthodes WMI peuvent retourner des collections volumineuses, provoquant ainsi un blocage des scripts.</span><span class="sxs-lookup"><span data-stu-id="f28eb-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="f28eb-105">Dans le script, l’accès semi-synchrone est la valeur par défaut, et Windows Management Instrumentation (WMI) définit **wbemFlagReturnImmediately** pour les appels qui peuvent retourner des collections d’objets volumineuses, telles que les méthodes [**SWbemServices**](swbemservices.md) suivantes : [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)et [**ReferencesTo**](swbemservices-referencesto.md).</span><span class="sxs-lookup"><span data-stu-id="f28eb-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="f28eb-106">L’accès semi-synchrone qui utilise **wbemFlagReturnImmediately** défini dans le paramètre *IFlags* est également la valeur par défaut pour les appels qui peuvent retourner des jeux d’objets volumineux pour les méthodes [**SWbemObject**](swbemobject.md) suivantes : [**instances \_**](swbemobject-instances-.md), [**sous-classes \_**](swbemobject-subclasses-.md), [**\_ associateurs**](swbemobject-associators-.md)et [**références \_**](swbemobject-references-.md).</span><span class="sxs-lookup"><span data-stu-id="f28eb-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="f28eb-107">Pour réduire l’utilisation des ressources de mémoire WMI lors du traitement d’une grande collection d’objets, incluez la valeur de **wbemFlagForwardOnly** dans le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="f28eb-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="f28eb-108">L’utilisation de **wbemFlagForwardOnly** amène WMI à créer un énumérateur avant uniquement qui ne permet pas de rembobiner la collection et d’accéder de nouveau aux éléments.</span><span class="sxs-lookup"><span data-stu-id="f28eb-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="f28eb-109">WMI élimine la mémoire pour chaque objet lorsque l’instruction **for each** traite un objet.</span><span class="sxs-lookup"><span data-stu-id="f28eb-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="f28eb-110">Vous ne pouvez pas appeler la méthode **Count** pour une collection lorsque l’indicateur **wbemFlagForwardOnly** a été défini sur l’appel qui a obtenu la collection.</span><span class="sxs-lookup"><span data-stu-id="f28eb-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="f28eb-111">Notez que le paramètre *IFlags* a **wbemFlagReturnImmediately** et **wbemFlagForwardOnly** définis par défaut pour la méthode [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="f28eb-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="f28eb-112">La procédure suivante décrit comment utiliser VBScript pour effectuer un appel semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="f28eb-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="f28eb-113">**Pour effectuer un appel semi-synchrone dans VBScript**</span><span class="sxs-lookup"><span data-stu-id="f28eb-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="f28eb-114">Définissez le paramètre *IFlags* sur la valeur de [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="f28eb-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="f28eb-115">Effectuez l’appel synchrone normal pour [**SWbemServices.ExecQuery**](swbemservices-execquery.md) ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) avec la valeur *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="f28eb-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="f28eb-116">Si vous souhaitez traiter les objets retournés par l’appel comme une collection, utilisez une syntaxe d’énumération telle que VBScript **pour chaque**.</span><span class="sxs-lookup"><span data-stu-id="f28eb-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="f28eb-117">À mesure que chaque objet est retourné, il est traité en tant qu’élément suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="f28eb-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="f28eb-118">Créez un énumérateur avant uniquement en associant la valeur de **wbemFlagReturnImmediately** à la valeur de **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="f28eb-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="f28eb-119">La valeur décimale de cette opération ou est 48.</span><span class="sxs-lookup"><span data-stu-id="f28eb-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="f28eb-120">Ces constantes sont définies dans la bibliothèque de types wbemdisp. tlb pour Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f28eb-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="f28eb-121">La plupart des langages de script utilisent la valeur numérique ou définissent une constante.</span><span class="sxs-lookup"><span data-stu-id="f28eb-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="f28eb-122">Pour plus d’informations, consultez [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="f28eb-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="f28eb-123">L’exemple de code suivant montre comment effectuer un appel de méthode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="f28eb-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="f28eb-124">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f28eb-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="f28eb-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f28eb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f28eb-126">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="f28eb-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



