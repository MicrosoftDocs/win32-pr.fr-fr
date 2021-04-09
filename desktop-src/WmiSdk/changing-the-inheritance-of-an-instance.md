---
description: Vous pouvez trouver une situation dans laquelle une instance qui a été créée en tant qu’enfant d’une classe parente doit modifier les classes parentes et devenir l’enfant d’une autre classe parente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Modification de l’héritage d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865677"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="26554-103">Modification de l’héritage d’une instance</span><span class="sxs-lookup"><span data-stu-id="26554-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="26554-104">Vous pouvez trouver une situation dans laquelle une instance qui a été créée en tant qu’enfant d’une classe parente doit modifier les classes parentes et devenir l’enfant d’une autre classe parente.</span><span class="sxs-lookup"><span data-stu-id="26554-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="26554-105">Par exemple, vous pouvez avoir une classe dérivée, **ManualService**, décrivant un service manuel, et une classe dérivée, **Autoservice**, décrivant un service automatique.</span><span class="sxs-lookup"><span data-stu-id="26554-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="26554-106">Les deux classes ont un grand nombre de propriétés.</span><span class="sxs-lookup"><span data-stu-id="26554-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="26554-107">Toutes les propriétés ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="26554-107">Not all properties are identical.</span></span> <span data-ttu-id="26554-108">Pour passer d’un service manuel à un service automatique, vous devez également remplacer l’instance de **ManualService** qui représente le service par **Autoservice**.</span><span class="sxs-lookup"><span data-stu-id="26554-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="26554-109">Dans la version actuelle de WMI, vous ne pouvez pas appeler la méthode [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) avec le paramètre *Pint* qui pointe vers une instance d' **Autoservice** et les propriétés de clé qui décrivent l’instance **ManualService** .</span><span class="sxs-lookup"><span data-stu-id="26554-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="26554-110">Si vous le faites, vous supprimez implicitement l’instance **ManualService** d’origine.</span><span class="sxs-lookup"><span data-stu-id="26554-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="26554-111">En résumé, une fois que vous avez établi la classe d’une instance, vous pouvez uniquement modifier la classe parente d’une instance en supprimant l’instance et en recréant l’instance en tant qu’instance de la nouvelle classe parente.</span><span class="sxs-lookup"><span data-stu-id="26554-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="26554-112">La procédure suivante décrit comment déplacer une instance d’une classe vers une autre.</span><span class="sxs-lookup"><span data-stu-id="26554-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="26554-113">**Pour déplacer une instance d’une classe vers une autre classe**</span><span class="sxs-lookup"><span data-stu-id="26554-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="26554-114">Supprimez l’instance de la classe d’origine.</span><span class="sxs-lookup"><span data-stu-id="26554-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="26554-115">Créez l’instance sous la nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="26554-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="26554-116">WMI n’autorise pas les applications à déplacer une instance en la créant dans la nouvelle classe, puis en la mettant à jour avec la clé de l’instance d’origine.</span><span class="sxs-lookup"><span data-stu-id="26554-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="26554-117">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="26554-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



