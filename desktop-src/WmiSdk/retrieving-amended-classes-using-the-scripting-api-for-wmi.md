---
description: Si vous utilisez l’API de script pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le cadre d’un moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Récupération des classes modifiées à l’aide de l’API de script pour WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543484"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="5c912-103">Récupération des classes modifiées à l’aide de l’API de script pour WMI</span><span class="sxs-lookup"><span data-stu-id="5c912-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="5c912-104">Si vous utilisez l’API de script pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le cadre d’un moniker.</span><span class="sxs-lookup"><span data-stu-id="5c912-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="5c912-105">Ou vous pouvez fournir le nom des paramètres régionaux dans le paramètre *strLocale* à la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="5c912-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="5c912-106">Lors de la lecture ou de l’écriture de classes amendées, indiquez que vous souhaitez utiliser les définitions de classe localisées en spécifiant [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) comme indicateur pour le paramètre *IFlags* de la méthode que vous appelez.</span><span class="sxs-lookup"><span data-stu-id="5c912-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="5c912-107">Pour PowerShell, vous pouvez utiliser le paramètre *-locale* sur [obtenir-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) pour spécifier les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="5c912-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="5c912-108">L’exemple de code suivant montre comment récupérer une classe localisée à l’aide d’un moniker de script WMI ou du paramètre-locale.</span><span class="sxs-lookup"><span data-stu-id="5c912-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="5c912-109">L’exemple de code suivant montre comment définir les paramètres régionaux et utiliser l’indicateur [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="5c912-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="5c912-110">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5c912-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="5c912-111">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c912-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="5c912-112">Le tableau suivant répertorie les méthodes qui acceptent l’indicateur [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="5c912-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="5c912-113">Méthode synchrone</span><span class="sxs-lookup"><span data-stu-id="5c912-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="5c912-114">Méthode asynchrone</span><span class="sxs-lookup"><span data-stu-id="5c912-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="5c912-115">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="5c912-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="5c912-116">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="5c912-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="5c912-117">**SWbemObject. Subclasses\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="5c912-118">**SWbemObject. SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="5c912-119">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="5c912-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="5c912-120">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="5c912-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="5c912-121">**SWbemObject. instances\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="5c912-122">**SWbemObject. InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="5c912-123">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="5c912-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="5c912-124">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="5c912-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="5c912-125">**SWbemServices.**</span><span class="sxs-lookup"><span data-stu-id="5c912-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="5c912-126">**SWbemServices. GetAsync**</span><span class="sxs-lookup"><span data-stu-id="5c912-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="5c912-127">**SWbemObject. put\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="5c912-128">**SWbemObject. PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="5c912-129">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="5c912-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="5c912-130">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="5c912-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="5c912-131">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="5c912-132">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="5c912-133">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="5c912-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="5c912-134">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="5c912-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="5c912-135">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="5c912-136">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="5c912-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
