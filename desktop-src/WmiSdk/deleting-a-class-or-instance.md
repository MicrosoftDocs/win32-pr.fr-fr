---
description: Une fois que vous avez terminé avec une classe ou une instance, vous souhaiterez peut-être supprimer cette classe ou cette instance de WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Suppression d’une classe ou d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202294"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="34446-103">Suppression d’une classe ou d’une instance</span><span class="sxs-lookup"><span data-stu-id="34446-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="34446-104">Une fois que vous avez terminé avec une classe ou une instance, vous souhaiterez peut-être supprimer cette classe ou cette instance de WMI.</span><span class="sxs-lookup"><span data-stu-id="34446-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="34446-105">Comme d’autres technologies orientées objet, vous pouvez supprimer des objets de classe ou d’instance pour nettoyer l’espace de noms WMI et pour retourner des ressources système.</span><span class="sxs-lookup"><span data-stu-id="34446-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="34446-106">Toutefois, de nombreuses classes et instances de WMI sont persistantes et utilisées par diverses applications à un moment donné. par conséquent, soyez prudent lors de la suppression d’une classe ou d’une instance WMI : votre application ou une autre application aura probablement besoin de la classe ou de l’instance à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="34446-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="34446-107">La suppression d’une classe ou d’une instance est une procédure simple.</span><span class="sxs-lookup"><span data-stu-id="34446-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="34446-108">Toutefois, en raison de la nature permanente d’une classe, vous n’aurez probablement pas besoin de supprimer une classe souvent.</span><span class="sxs-lookup"><span data-stu-id="34446-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="34446-109">Par exemple, il est peu probable que vous supprimiez la classe [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , car il est peu probable que vous ne disposiez pas d’un lecteur de disque au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="34446-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="34446-110">Au lieu de cela, vous serez plus enclin à supprimer une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="34446-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="34446-111">Pour plus d’informations, consultez [Suppression d’une instance](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="34446-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="34446-112">Bien que cela soit rare, vous pouvez être amené à mettre à jour une classe que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="34446-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="34446-113">Par exemple, vous pouvez créer une classe pour représenter une application tierce.</span><span class="sxs-lookup"><span data-stu-id="34446-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="34446-114">Si le logiciel tiers a mis à jour ses logiciels dans la mesure où votre classe n’est plus correctement représentée par le logiciel, vous devrez peut-être supprimer votre classe d’origine.</span><span class="sxs-lookup"><span data-stu-id="34446-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="34446-115">Pour plus d’informations, consultez [Suppression d’une classe](deleting-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="34446-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34446-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34446-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34446-117">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="34446-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
