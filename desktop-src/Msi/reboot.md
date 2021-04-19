---
description: La propriété reboot supprime certaines invites pour un redémarrage du système.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526538"
---
# <a name="reboot-property"></a><span data-ttu-id="d1b44-103">Reboot, propriété</span><span class="sxs-lookup"><span data-stu-id="d1b44-103">REBOOT property</span></span>

<span data-ttu-id="d1b44-104">La propriété **reboot** supprime certaines invites pour un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="d1b44-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="d1b44-105">Un administrateur utilise généralement cette propriété avec une série d’installations pour installer plusieurs produits en même temps avec un seul redémarrage à la fin.</span><span class="sxs-lookup"><span data-stu-id="d1b44-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="d1b44-106">Pour plus d’informations, consultez [redémarrages du système](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="d1b44-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="d1b44-107">Les actions [ForceReboot](forcereboot-action.md) et [ScheduleReboot](schedulereboot-action.md) indiquent au programme d’installation d’inviter l’utilisateur à redémarrer le système.</span><span class="sxs-lookup"><span data-stu-id="d1b44-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="d1b44-108">Le programme d’installation peut également déterminer qu’un redémarrage est nécessaire, qu’il y ait des actions ForceReboot ou ScheduleReboot dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="d1b44-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="d1b44-109">Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers en cours d’utilisation pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="d1b44-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="d1b44-110">Vous pouvez supprimer certaines invites pour les redémarrages en définissant la propriété **reboot** comme suit.</span><span class="sxs-lookup"><span data-stu-id="d1b44-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="d1b44-111">Valeur de redémarrage</span><span class="sxs-lookup"><span data-stu-id="d1b44-111">REBOOT value</span></span>   | <span data-ttu-id="d1b44-112">Description</span><span class="sxs-lookup"><span data-stu-id="d1b44-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b44-113">Force</span><span class="sxs-lookup"><span data-stu-id="d1b44-113">Force</span></span>          | <span data-ttu-id="d1b44-114">Toujours demander un redémarrage à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d1b44-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="d1b44-115">L’interface utilisateur invite toujours l’utilisateur à redémarrer à la fin.</span><span class="sxs-lookup"><span data-stu-id="d1b44-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="d1b44-116">S’il n’existe pas d’interface utilisateur et qu’il ne s’agit pas d’une [installation de plusieurs packages](multiple-package-installations.md), le système redémarre automatiquement à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d1b44-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="d1b44-117">S’il s’agit d’une installation de plusieurs packages, il n’y a pas de redémarrage automatique du système et le programme d’installation retourne l’erreur \_ redémarrage de la réussite \_ \_ obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d1b44-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="d1b44-118">Suppress</span><span class="sxs-lookup"><span data-stu-id="d1b44-118">Suppress</span></span>       | <span data-ttu-id="d1b44-119">Supprimer les invites de redémarrage à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d1b44-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="d1b44-120">Le programme d’installation invite toujours l’utilisateur à redémarrer au cours de l’installation chaque fois qu’il rencontre l' [action ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="d1b44-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="d1b44-121">S’il n’existe pas d’interface utilisateur, le système redémarre automatiquement à chaque ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="d1b44-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="d1b44-122">Le redémarrage à la fin de l’installation (par exemple, dû à une tentative d’installation d’un fichier en cours d’utilisation) est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d1b44-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="d1b44-123">ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="d1b44-123">ReallySuppress</span></span> | <span data-ttu-id="d1b44-124">Supprimez tous les redémarrages et redémarrez les invites lancées par ForceReboot lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d1b44-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="d1b44-125">À la fin de l’installation, supprimez tous les redémarrages et redémarrez les invites.</span><span class="sxs-lookup"><span data-stu-id="d1b44-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="d1b44-126">L’invite de redémarrage et le redémarrage proprement dit sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="d1b44-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="d1b44-127">Par exemple, le redémarrage à la fin de l’installation, provoqué par une tentative d’installation d’un fichier en cours d’utilisation, est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d1b44-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="d1b44-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d1b44-128">Remarks</span></span>

<span data-ttu-id="d1b44-129">Le programme d’installation évalue uniquement le premier caractère de la propriété **reboot** .</span><span class="sxs-lookup"><span data-stu-id="d1b44-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b44-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1b44-130">Requirements</span></span>



| <span data-ttu-id="d1b44-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1b44-131">Requirement</span></span> | <span data-ttu-id="d1b44-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1b44-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b44-133">Version</span><span class="sxs-lookup"><span data-stu-id="d1b44-133">Version</span></span><br/> | <span data-ttu-id="d1b44-134">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1b44-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d1b44-135">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d1b44-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d1b44-136">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1b44-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d1b44-137">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b44-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1b44-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1b44-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b44-139">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1b44-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d1b44-140">**Propriété REBOOTPROMPT**</span><span class="sxs-lookup"><span data-stu-id="d1b44-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="d1b44-141">Redémarrages du système</span><span class="sxs-lookup"><span data-stu-id="d1b44-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




