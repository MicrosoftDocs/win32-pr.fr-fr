---
description: En plus des classes et des instances, WMI vous permet de modifier une méthode. La principale raison pour laquelle vous souhaitez modifier une méthode est si vous avez modifié l’implémentation d’une méthode dans un fournisseur. Pour plus d’informations, consultez écriture d’un fournisseur de méthodes.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modification d’une méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393328"
---
# <a name="modifying-a-method"></a><span data-ttu-id="b65f4-105">Modification d’une méthode</span><span class="sxs-lookup"><span data-stu-id="b65f4-105">Modifying a Method</span></span>

<span data-ttu-id="b65f4-106">En plus des classes et des instances, WMI vous permet de modifier une méthode.</span><span class="sxs-lookup"><span data-stu-id="b65f4-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="b65f4-107">La principale raison pour laquelle vous souhaitez modifier une méthode est si vous avez modifié l’implémentation d’une méthode dans un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b65f4-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="b65f4-108">Pour plus d’informations, consultez [écriture d’un fournisseur de méthodes](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b65f4-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="b65f4-109">La modification d’une méthode n’est pas une opération qui peut être effectuée dans un script.</span><span class="sxs-lookup"><span data-stu-id="b65f4-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="b65f4-110">La procédure suivante décrit comment modifier une méthode par programme.</span><span class="sxs-lookup"><span data-stu-id="b65f4-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="b65f4-111">**Pour modifier une méthode par programmation**</span><span class="sxs-lookup"><span data-stu-id="b65f4-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="b65f4-112">Récupérez la définition de classe avec un appel à [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span><span class="sxs-lookup"><span data-stu-id="b65f4-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="b65f4-113">Les deux paramètres out, *ppInSignature* et *ppOutSignature*, contiennent respectivement la classe in-Parameter et la classe out-Parameter.</span><span class="sxs-lookup"><span data-stu-id="b65f4-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="b65f4-114">La valeur de retour est regroupée dans la classe de paramètres de sortie en tant que propriété et doit être nommée **returnValue**.</span><span class="sxs-lookup"><span data-stu-id="b65f4-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="b65f4-115">Récupérez et modifiez les paramètres avec des appels à [**IWbemClassObject :: obten**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)ou [**IWbemClassObject ::D supprim**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span><span class="sxs-lookup"><span data-stu-id="b65f4-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="b65f4-116">Placez votre nouvelle version de la méthode dans la classe parente à l’aide d’un appel à [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="b65f4-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="b65f4-117">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="b65f4-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



