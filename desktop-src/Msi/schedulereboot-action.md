---
description: Insérez l’action ScheduleReboot dans la séquence d’action pour inviter l’utilisateur à redémarrer le système à la fin de l’installation. Utilisez l’action ForceReboot pour demander un redémarrage lors de l’installation.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Action ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865197"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="68e91-104">Action ScheduleReboot</span><span class="sxs-lookup"><span data-stu-id="68e91-104">ScheduleReboot Action</span></span>

<span data-ttu-id="68e91-105">Insérez l’action ScheduleReboot dans la séquence d’action pour inviter l’utilisateur à redémarrer le système à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="68e91-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="68e91-106">Utilisez l' [action ForceReboot](forcereboot-action.md) pour demander un redémarrage lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="68e91-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="68e91-107">Si l’installation a une interface utilisateur, le programme d’installation affiche une boîte de message et un bouton à la fin de l’installation, en demandant si l’utilisateur souhaite redémarrer le système.</span><span class="sxs-lookup"><span data-stu-id="68e91-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="68e91-108">L’utilisateur doit répondre à cette invite avant de terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="68e91-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="68e91-109">Si l’installation n’a pas d’interface utilisateur, le système redémarre automatiquement à la fin.</span><span class="sxs-lookup"><span data-stu-id="68e91-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="68e91-110">Si le programme d’installation détermine qu’un redémarrage est nécessaire, il invite automatiquement l’utilisateur à redémarrer à la fin de l’installation, qu’il y ait ou non des actions ForceReboot ou ScheduleReboot dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="68e91-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="68e91-111">Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers en cours d’utilisation pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="68e91-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="68e91-112">Vous pouvez supprimer certaines invites pour les redémarrages en définissant la propriété [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="68e91-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="68e91-113">Si le Windows Installer rencontre l’action [ForceReboot](forcereboot-action.md) ou ScheduleReboot lors d’une [installation de plusieurs packages](multiple-package-installations.md), le programme d’installation s’arrête et annule l’installation.</span><span class="sxs-lookup"><span data-stu-id="68e91-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="68e91-114">D’autres packages appartenant à l’installation de plusieurs packages, qui ne contiennent pas d’action ForceReboot ou ScheduleReboot, peuvent être installés.</span><span class="sxs-lookup"><span data-stu-id="68e91-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="68e91-115">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="68e91-115">Sequence Restrictions</span></span>

<span data-ttu-id="68e91-116">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="68e91-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="68e91-117">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="68e91-117">ActionData Messages</span></span>

<span data-ttu-id="68e91-118">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="68e91-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e91-119">Notes</span><span class="sxs-lookup"><span data-stu-id="68e91-119">Remarks</span></span>

<span data-ttu-id="68e91-120">Par exemple, cette action peut être utilisée pour forcer le programme d’installation à demander un redémarrage après l’installation des pilotes qui nécessitent un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="68e91-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="68e91-121">Si le programme d’installation tente de remplacer des fichiers qui sont en cours d’utilisation, il invite automatiquement l’utilisateur à redémarrer même si ScheduleReboot n’a pas été utilisé.</span><span class="sxs-lookup"><span data-stu-id="68e91-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="68e91-122">L’action ScheduleReboot est généralement placée à la fin de la séquence, mais elle peut être insérée à n’importe quel point de la séquence.</span><span class="sxs-lookup"><span data-stu-id="68e91-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68e91-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68e91-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68e91-124">Redémarrages du système</span><span class="sxs-lookup"><span data-stu-id="68e91-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



