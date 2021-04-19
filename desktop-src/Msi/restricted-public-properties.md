---
description: Dans certains cas, un utilisateur qui n’est pas un administrateur système ne peut pas remplacer une liste approuvée de propriétés publiques Windows Installer limitées.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propriétés publiques restreintes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530889"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="de151-103">Propriétés publiques restreintes</span><span class="sxs-lookup"><span data-stu-id="de151-103">Restricted Public Properties</span></span>

<span data-ttu-id="de151-104">Dans le cas d’une installation gérée, l’auteur du package peut avoir besoin de limiter les [propriétés publiques](public-properties.md) qui sont transmises côté serveur et peut être modifiée par un utilisateur qui n’est pas un administrateur système.</span><span class="sxs-lookup"><span data-stu-id="de151-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="de151-105">Certaines restrictions sont généralement nécessaires pour maintenir un environnement sécurisé lorsque l’installation requiert que le programme d’installation utilise des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="de151-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="de151-106">Si toutes les conditions suivantes sont réunies, un utilisateur qui n’est pas un administrateur système peut uniquement remplacer une liste approuvée de propriétés publiques restreintes :</span><span class="sxs-lookup"><span data-stu-id="de151-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="de151-107">Le système est Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="de151-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="de151-108">L’utilisateur n’est pas un administrateur système.</span><span class="sxs-lookup"><span data-stu-id="de151-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="de151-109">L’application ou le produit est en cours d’installation avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="de151-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="de151-110">Si toutes les conditions ci-dessus sont vraies, le programme d’installation se trouve par défaut dans la liste suivante de propriétés publiques restreintes qui peuvent être modifiées par n’importe quel utilisateur :</span><span class="sxs-lookup"><span data-stu-id="de151-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="de151-111">**TRANSACTIONNEL**</span><span class="sxs-lookup"><span data-stu-id="de151-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="de151-112">**AFTERREBOOT**</span><span class="sxs-lookup"><span data-stu-id="de151-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="de151-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="de151-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="de151-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="de151-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="de151-115">**EXECUTEMODE**</span><span class="sxs-lookup"><span data-stu-id="de151-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="de151-116">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="de151-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="de151-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="de151-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="de151-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="de151-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="de151-119">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="de151-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="de151-120">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="de151-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="de151-121">**LOGACTION**</span><span class="sxs-lookup"><span data-stu-id="de151-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="de151-122">**NOCOMPANYNAME**</span><span class="sxs-lookup"><span data-stu-id="de151-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="de151-123">**NOM de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="de151-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="de151-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span><span class="sxs-lookup"><span data-stu-id="de151-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="de151-125">**MSIINSTANCEGUID**</span><span class="sxs-lookup"><span data-stu-id="de151-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="de151-126">**MSINEWINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="de151-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="de151-127">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="de151-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="de151-128">**CORRECTIF**</span><span class="sxs-lookup"><span data-stu-id="de151-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="de151-129">**PRIMARYFOLDER**</span><span class="sxs-lookup"><span data-stu-id="de151-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="de151-130">**PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="de151-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="de151-131">**INITIAL**</span><span class="sxs-lookup"><span data-stu-id="de151-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="de151-132">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="de151-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="de151-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="de151-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="de151-134">**RESUME**</span><span class="sxs-lookup"><span data-stu-id="de151-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="de151-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="de151-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="de151-136">**SHORTFILENAMES**</span><span class="sxs-lookup"><span data-stu-id="de151-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="de151-137">**TRANSFORMATIONS**</span><span class="sxs-lookup"><span data-stu-id="de151-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="de151-138">**TRANSFORMSATSOURCE**</span><span class="sxs-lookup"><span data-stu-id="de151-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="de151-139">L’auteur d’un package d’installation peut étendre cette liste par défaut pour inclure des propriétés publiques supplémentaires à l’aide de la propriété [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="de151-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="de151-140">La définition de la propriété [**EnableUserControl**](-enableusercontrol.md) ou de la [stratégie système](system-policy.md) [EnableUserControl](enableusercontrol.md)étend la liste à toutes les propriétés publiques.</span><span class="sxs-lookup"><span data-stu-id="de151-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="de151-141">Tous les utilisateurs peuvent ensuite modifier toute propriété publique.</span><span class="sxs-lookup"><span data-stu-id="de151-141">All users can then change any public property.</span></span>

<span data-ttu-id="de151-142">Le programme d’installation définit la propriété [**RestrictedUserControl**](restrictedusercontrol.md) chaque fois que la liste des propriétés publiques transmises au serveur par des utilisateurs non-administrateurs est limitée.</span><span class="sxs-lookup"><span data-stu-id="de151-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de151-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de151-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de151-144">À propos des propriétés</span><span class="sxs-lookup"><span data-stu-id="de151-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



