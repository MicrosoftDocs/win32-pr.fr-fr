---
description: Le programme d’installation définit la propriété OutOfNoRbDiskSpace sur true si un volume qui est une cible de l’installation ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propriété OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541642"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="03808-103">Propriété OutOfNoRbDiskSpace</span><span class="sxs-lookup"><span data-stu-id="03808-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="03808-104">Le programme d’installation définit la propriété **OutOfNoRbDiskSpace** sur true si un volume qui est une cible de l’installation ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation.</span><span class="sxs-lookup"><span data-stu-id="03808-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="03808-105">Dans ce cas, la propriété **OutOfNoRbDiskSpace** est définie sur true même si la restauration a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="03808-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="03808-106">Si tous les volumes disposent de suffisamment d’espace, la valeur est false.</span><span class="sxs-lookup"><span data-stu-id="03808-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="03808-107">Un développeur d’un package d’installation peut gérer la situation lorsque la propriété [**OutOfDiskSpace**](outofdiskspace.md) a la valeur true et que la propriété **OutOfNoRbDiskSpace** a la valeur false en créant une interface utilisateur qui présente à l’utilisateur une option permettant de désactiver la restauration et de poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="03808-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="03808-108">Pour plus d’informations sur l’affichage conditionnel d’une boîte de dialogue, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="03808-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="03808-109">Pour plus d’informations sur la désactivation de la restauration, consultez [EnableRollback ControlEvent,](enablerollback-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="03808-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="03808-110">La propriété **OutOfNoRbDiskSpace** est valide à tout moment après l’exécution de l' [action CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="03808-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="03808-111">L’état de la propriété **OutOfNoRbDiskSpace** est mis à jour de manière dynamique chaque fois que le coût total d’installation est recalculé (par exemple, chaque fois que l’état d’installation d’une fonctionnalité est modifié via la [boîte de dialogue de sélection](selection-dialog.md)).</span><span class="sxs-lookup"><span data-stu-id="03808-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="03808-112">Les actions de résolution de sélection utilisent cette valeur pour annuler une installation et générer une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="03808-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="03808-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03808-113">Requirements</span></span>



| <span data-ttu-id="03808-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03808-114">Requirement</span></span> | <span data-ttu-id="03808-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="03808-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03808-116">Version</span><span class="sxs-lookup"><span data-stu-id="03808-116">Version</span></span><br/> | <span data-ttu-id="03808-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03808-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03808-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03808-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03808-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="03808-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="03808-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="03808-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03808-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03808-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03808-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03808-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="03808-123">Présentation de ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="03808-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="03808-124">**Propriété OutOfDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="03808-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="03808-125">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="03808-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="03808-126">Action CostFinalize</span><span class="sxs-lookup"><span data-stu-id="03808-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="03808-127">Boîte de dialogue de sélection</span><span class="sxs-lookup"><span data-stu-id="03808-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




