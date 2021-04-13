---
description: 'Les méthodes IWbemServices :: ExecMethod ou ExecMethodAsync requièrent la \_ \_ classe système Parameters en tant que conteneur dans pInParams si la méthode qu’elles exécutent possède des arguments d’entrée.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Création d’objets de paramètres en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202297"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="b79fb-103">Création d’objets de paramètres en C++</span><span class="sxs-lookup"><span data-stu-id="b79fb-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="b79fb-104">Les méthodes [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) requièrent la classe système [**\_ \_ Parameters**](--parameters.md) en tant que conteneur dans *pInParams* si la méthode qu’elles exécutent possède des arguments d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b79fb-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="b79fb-105">La procédure suivante décrit comment créer une instance de la classe système [**\_ \_ Parameters**](--parameters.md) pour contenir les informations sur les paramètres.</span><span class="sxs-lookup"><span data-stu-id="b79fb-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="b79fb-106">**Pour créer une instance de \_ \_ paramètres**</span><span class="sxs-lookup"><span data-stu-id="b79fb-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="b79fb-107">Déterminez le chemin d’accès de la classe contenant la définition de la méthode.</span><span class="sxs-lookup"><span data-stu-id="b79fb-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="b79fb-108">En utilisant le chemin de classe et le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) transmis à partir de [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), appelez [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) pour récupérer les classes de paramètres d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="b79fb-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="b79fb-109">La méthode [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retourne un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pour accéder à chacune de ces classes.</span><span class="sxs-lookup"><span data-stu-id="b79fb-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="b79fb-110">À l’aide du pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pour la classe de sortie, appelez [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) pour créer une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="b79fb-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="b79fb-111">Remplissez l’instance de classe en définissant les propriétés qui correspondent aux valeurs de sortie et, s’il existe une valeur de retour pour la méthode, la propriété [returnValue](creating-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b79fb-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="b79fb-112">Transmettez l’instance de [**\_ \_ paramètres**](--parameters.md) à l’appelant par le biais de la méthode [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="b79fb-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="b79fb-113">Une fois que le fournisseur de méthode a déterminé que les paramètres d’entrée sont corrects, la méthode vers laquelle pointe *strMethodName* peut toujours réussir ou échouer.</span><span class="sxs-lookup"><span data-stu-id="b79fb-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="b79fb-114">Certains fournisseurs de méthode génèrent un deuxième thread pour implémenter la méthode afin que la réussite ou l’échec réel de la méthode finit par être signalé à l’appelant via [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="b79fb-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="b79fb-115">Notez que **IWbemObjectSink :: SetStatus** ne reçoit pas le code de retour de la méthode du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b79fb-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="b79fb-116">Toutefois, elle reçoit le code de retour du mécanisme réel de retour d’appel et est utile uniquement pour vérifier que l’appel s’est produit ou qu’il a échoué pour des raisons mécaniques.</span><span class="sxs-lookup"><span data-stu-id="b79fb-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b79fb-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b79fb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b79fb-118">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="b79fb-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="b79fb-119">**IWbemCallResult::GetResultObject**</span><span class="sxs-lookup"><span data-stu-id="b79fb-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="b79fb-120">**IWbemServices :: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="b79fb-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="b79fb-121">**IWbemServices :: ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="b79fb-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



