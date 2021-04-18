---
description: La suppression d’une instance est la commande de suppression la plus courante que vous êtes susceptible d’effectuer dans WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Suppression d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519840"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="7ddb1-103">Suppression d’une instance</span><span class="sxs-lookup"><span data-stu-id="7ddb1-103">Deleting an Instance</span></span>

<span data-ttu-id="7ddb1-104">La suppression d’une instance est la commande de suppression la plus courante que vous êtes susceptible d’effectuer dans WMI.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="7ddb1-105">À l’instar de la suppression d’une classe, la commande réelle est assez simple.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="7ddb1-106">Toutefois, WMI fonctionne de façon très différente selon le type d’instance que vous supprimez.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="7ddb1-107">Si l’instance est statique, WMI supprime simplement l’instance de l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="7ddb1-108">Pour plus d’informations sur la suppression de classes et d’instances de l’espace de stockage WMI, consultez la commande de préprocesseur [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="7ddb1-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="7ddb1-109">Si l’instance est dynamique, WMI doit appeler [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) sur les fournisseurs qui sont responsables des classes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ddb1-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="7ddb1-110">Classe qui possède l’instance de.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="7ddb1-111">Chaque classe parente de la classe qui possède l’instance de.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="7ddb1-112">Chaque sous-classe de la classe qui possède l’instance.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="7ddb1-113">La réussite de la suppression dépend de la classe non abstraite la plus grande pour l’instance d’origine.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="7ddb1-114">Si le fournisseur de toute classe non abstraite de niveau supérieur réussit à terminer la suppression, l’opération réussit.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="7ddb1-115">Pour plus d’informations, consultez la section Notes de [**IWbemServices ::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span><span class="sxs-lookup"><span data-stu-id="7ddb1-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="7ddb1-116">L' [API com pour WMI](com-api-for-wmi.md) a différentes méthodes pour supprimer une instance et supprimer un objet.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="7ddb1-117">La procédure suivante décrit comment utiliser C++ pour supprimer une instance d’une classe de base ou d’une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="7ddb1-118">**Pour supprimer une instance d’une classe de base ou d’une classe dérivée à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="7ddb1-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="7ddb1-119">Appelez les méthodes [**IWbemServices ::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) ou [**IWbemServices ::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="7ddb1-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="7ddb1-120">Comme son nom l’indique, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) supprime une instance de façon asynchrone tandis que [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) supprime une instance de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="7ddb1-121">Pour utiliser **DeleteInstanceAsync**, vous devez également implémenter un objet [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="7ddb1-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="7ddb1-122">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="7ddb1-123">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ddb1-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="7ddb1-124">L' [API de script pour WMI](scripting-api-for-wmi.md) utilise les mêmes méthodes pour supprimer un objet de classe ou une instance.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="7ddb1-125">La procédure suivante décrit comment utiliser VBScript pour supprimer une instance d’une classe de base ou d’une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="7ddb1-126">**Pour supprimer une instance d’une classe de base ou d’une classe dérivée à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="7ddb1-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="7ddb1-127">Appelez les méthodes [**SWbemObject. Delete \_**](swbemobject-delete-.md) ou [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="7ddb1-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="7ddb1-128">Comme son nom l’indique [**, \_ Delete**](swbemobject-delete-.md) supprime une instance de façon synchrone, tandis que [**DeleteAsync \_**](swbemobject-deleteasync-.md) supprime une instance de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="7ddb1-129">Pour plus d’informations sur la suppression d’une instance de façon asynchrone, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ddb1-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="7ddb1-130">L’exemple suivant décrit comment supprimer une instance de à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="7ddb1-131">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7ddb1-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="7ddb1-132">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ddb1-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



