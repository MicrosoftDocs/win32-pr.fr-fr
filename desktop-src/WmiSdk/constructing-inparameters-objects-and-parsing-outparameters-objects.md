---
description: Normalement, l’accès direct est suffisant pour appeler une méthode de fournisseur WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construction d’objets Parameters et analyse d’objets de paramètres de paramétrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952469"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="3c5c8-103">Construction d’objets Parameters et analyse d’objets de paramètres de paramétrage</span><span class="sxs-lookup"><span data-stu-id="3c5c8-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="3c5c8-104">Normalement, l’accès direct est suffisant pour appeler une [*méthode de fournisseur*](gloss-p.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="3c5c8-105">L’accès direct implique l’exécution d’une méthode à l’aide de la syntaxe *Object. Method* .</span><span class="sxs-lookup"><span data-stu-id="3c5c8-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="3c5c8-106">Toutefois, dans certains cas, l’accès direct ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="3c5c8-107">En outre, l’appel d’une méthode de fournisseur de manière asynchrone à partir d’un script nécessite un type d’appel [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="3c5c8-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="3c5c8-108">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="3c5c8-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3c5c8-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="3c5c8-110">L’ordre des paramètres d’entrée et de sortie de la méthode est défini dans le schéma format MOF (MOF) de la méthode.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="3c5c8-111">WMI n’empêche pas la modification de l’ordre des paramètres lorsque la classe est recompilée par [mofcomp](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="3c5c8-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="3c5c8-112">En utilisant un objet [**Parameters**](swbemmethod-inparameters.md) , vous pouvez éviter les problèmes qui résultent d’un schéma modifié, car les paramètres d’entrée sont identifiés par leur nom.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="3c5c8-113">Le paramètre correct peut être consulté en examinant le qualificateur d' **ID** de chaque paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="3c5c8-114">Le premier paramètre a une valeur d' **ID** égale à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="3c5c8-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="3c5c8-115">[**Les méthodes SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)et [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) offrent un autre moyen d’exécuter une méthode de fournisseur dans les cas où il n’est pas possible d’exécuter directement une méthode.</span><span class="sxs-lookup"><span data-stu-id="3c5c8-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="3c5c8-116">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="3c5c8-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="3c5c8-117">Pour plus d’informations sur les paramètres, consultez [construction d’objets inparamètres](constructing-inparameters-objects.md) et [analyse d’objets de paramètres de paramètres](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3c5c8-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



