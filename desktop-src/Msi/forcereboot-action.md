---
description: L’action ForceReboot invite l’utilisateur à redémarrer le système pendant l’installation.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Action ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520012"
---
# <a name="forcereboot-action"></a><span data-ttu-id="492ff-103">Action ForceReboot</span><span class="sxs-lookup"><span data-stu-id="492ff-103">ForceReboot Action</span></span>

<span data-ttu-id="492ff-104">L’action ForceReboot invite l’utilisateur à redémarrer le système pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="492ff-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="492ff-105">L’action ForceReboot est différente de l' [action ScheduleReboot](schedulereboot-action.md) , car l’action ScheduleReboot est utilisée pour planifier une invite de redémarrage à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="492ff-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="492ff-106">Si l’installation a une interface utilisateur, le programme d’installation affiche une boîte de dialogue à chaque action ForceReboot qui invite l’utilisateur à redémarrer le système.</span><span class="sxs-lookup"><span data-stu-id="492ff-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="492ff-107">L’utilisateur doit répondre à cette invite avant de poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="492ff-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="492ff-108">Si l’installation n’a pas d’interface utilisateur, le système redémarre automatiquement à l’action ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="492ff-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="492ff-109">Si le programme d’installation détermine qu’un redémarrage est nécessaire, il invite automatiquement l’utilisateur à redémarrer à la fin de l’installation, qu’il y ait ou non des actions ForceReboot ou ScheduleReboot dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="492ff-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="492ff-110">Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers utilisés lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="492ff-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="492ff-111">Supprimez certaines invites de redémarrage en définissant la propriété [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="492ff-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="492ff-112">Si le Windows Installer rencontre l’action ForceReboot ou [ScheduleReboot](schedulereboot-action.md) lors d’une [installation de plusieurs packages](multiple-package-installations.md), le programme d’installation s’arrête et annule l’installation.</span><span class="sxs-lookup"><span data-stu-id="492ff-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="492ff-113">D’autres packages appartenant à l’installation de plusieurs packages, qui ne contiennent pas d’action ForceReboot ou ScheduleReboot, peuvent être installés.</span><span class="sxs-lookup"><span data-stu-id="492ff-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="492ff-114">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="492ff-114">Sequence Restrictions</span></span>

<span data-ttu-id="492ff-115">Les actions suivantes se produisent généralement ensemble en tant que groupe dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="492ff-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="492ff-116">Il est recommandé que l’action ForceReboot soit planifiée pour venir après ce groupe.</span><span class="sxs-lookup"><span data-stu-id="492ff-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="492ff-117">Si l’action ForceReboot est planifiée avant l' [action RegisterProduct](registerproduct-action.md), le programme d’installation requiert à nouveau la source du package d’installation après le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="492ff-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="492ff-118">Par conséquent, la séquence par défaut pour ForceReboot suit immédiatement cette séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="492ff-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="492ff-119">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="492ff-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="492ff-120">RegisterUser</span><span class="sxs-lookup"><span data-stu-id="492ff-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="492ff-121">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="492ff-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="492ff-122">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="492ff-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="492ff-123">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="492ff-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="492ff-124">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="492ff-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="492ff-125">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="492ff-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="492ff-126">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="492ff-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="492ff-127">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="492ff-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="492ff-128">L’action ForceReboot doit être comprise entre [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md) dans la séquence d’action de la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="492ff-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="492ff-129">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="492ff-129">ActionData Messages</span></span>

<span data-ttu-id="492ff-130">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="492ff-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="492ff-131">Notes</span><span class="sxs-lookup"><span data-stu-id="492ff-131">Remarks</span></span>

<span data-ttu-id="492ff-132">L’action ForceReboot doit toujours être utilisée avec une instruction conditionnelle de sorte que le programme d’installation déclenche un redémarrage uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="492ff-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="492ff-133">Par exemple, un redémarrage peut être nécessaire uniquement si un fichier particulier est remplacé ou si un composant particulier est installé.</span><span class="sxs-lookup"><span data-stu-id="492ff-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="492ff-134">Chaque installation de produit est unique et une action personnalisée peut être nécessaire pour déterminer si un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="492ff-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="492ff-135">La condition sur l’action ForceReboot utilise généralement la propriété [**AFTERREBOOT**](afterreboot.md) .</span><span class="sxs-lookup"><span data-stu-id="492ff-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="492ff-136">ForceReboot exécute les opérations système générées par les actions précédentes avant de demander un redémarrage ou un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="492ff-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="492ff-137">Par exemple, les opérations système générées par [InstallFiles](installfiles-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) sont exécutées avant un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="492ff-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="492ff-138">L’action ForceReboot écrit une clé de Registre qui entraîne le démarrage du programme d’installation après le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="492ff-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="492ff-139">L’emplacement de cette clé est **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.</span><span class="sxs-lookup"><span data-stu-id="492ff-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="492ff-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="492ff-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="492ff-141">Redémarrages du système</span><span class="sxs-lookup"><span data-stu-id="492ff-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



