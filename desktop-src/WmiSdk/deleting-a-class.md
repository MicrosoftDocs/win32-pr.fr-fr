---
description: Contrairement à la suppression d’une instance dynamique, la suppression d’une classe est une procédure simple.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Suppression d’une classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538698"
---
# <a name="deleting-a-class"></a><span data-ttu-id="3637f-103">Suppression d’une classe</span><span class="sxs-lookup"><span data-stu-id="3637f-103">Deleting a Class</span></span>

<span data-ttu-id="3637f-104">Contrairement à la suppression d’une instance dynamique, la suppression d’une classe est une procédure simple.</span><span class="sxs-lookup"><span data-stu-id="3637f-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="3637f-105">Toutefois, comme nous l’avons vu précédemment, les classes de base ou dérivées sont rarement supprimées.</span><span class="sxs-lookup"><span data-stu-id="3637f-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="3637f-106">Au lieu de cela, une instance est plus souvent supprimée.</span><span class="sxs-lookup"><span data-stu-id="3637f-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="3637f-107">L' [API de script pour WMI](scripting-api-for-wmi.md) utilise les mêmes méthodes pour supprimer un objet de classe ou une instance.</span><span class="sxs-lookup"><span data-stu-id="3637f-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="3637f-108">Pour plus d’informations, consultez [Suppression d’une instance](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="3637f-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="3637f-109">Pour plus d’informations sur la suppression de classes et d’instances de l’espace de stockage WMI, consultez la commande de préprocesseur [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="3637f-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="3637f-110">L' [API com pour WMI](com-api-for-wmi.md) a différentes méthodes pour supprimer une instance et supprimer un objet.</span><span class="sxs-lookup"><span data-stu-id="3637f-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="3637f-111">La procédure suivante décrit comment supprimer une classe de base ou une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="3637f-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="3637f-112">**Pour supprimer une classe de base ou une classe dérivée**</span><span class="sxs-lookup"><span data-stu-id="3637f-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="3637f-113">Appelez la méthode [**IWbemServices ::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) ou [**IWbemServices ::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .</span><span class="sxs-lookup"><span data-stu-id="3637f-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="3637f-114">Comme son nom l’indique, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) supprime une instance de façon asynchrone tandis que [**deleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) supprime une instance de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="3637f-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="3637f-115">Pour utiliser **DeleteClassAsync**, vous devez également implémenter un objet [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="3637f-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="3637f-116">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3637f-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="3637f-117">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3637f-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



