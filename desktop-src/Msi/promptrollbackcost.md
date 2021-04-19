---
description: La propriété PROMPTROLLBACKCOST spécifie l’action effectuée par le programme d’installation si les fonctionnalités d’annulation de la restauration sont activées et que l’espace disque est insuffisant pour terminer l’installation. Les valeurs possibles de PROMPTROLLBACKCOST sont les suivantes. ValueActionPDisplay boîte de dialogue qui vous demande s’il faut continuer sans restauration. DDisable Rollback et continue sans demander à l’utilisateur. FFail avec l’invite d’erreur d’espace disque insuffisant.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propriété PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531103"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="ed4af-103">Propriété PROMPTROLLBACKCOST</span><span class="sxs-lookup"><span data-stu-id="ed4af-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="ed4af-104">La propriété **PROMPTROLLBACKCOST** spécifie l’action effectuée par le programme d’installation si les fonctionnalités d’annulation de la [restauration](rollback-installation.md) sont activées et que l’espace disque est insuffisant pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="ed4af-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="ed4af-105">Les valeurs possibles de **PROMPTROLLBACKCOST** sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed4af-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="ed4af-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed4af-106">Value</span></span> | <span data-ttu-id="ed4af-107">Action</span><span class="sxs-lookup"><span data-stu-id="ed4af-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="ed4af-108">P</span><span class="sxs-lookup"><span data-stu-id="ed4af-108">P</span></span>     | <span data-ttu-id="ed4af-109">Affiche une boîte de dialogue qui vous demande s’il faut continuer sans restauration.</span><span class="sxs-lookup"><span data-stu-id="ed4af-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="ed4af-110">D</span><span class="sxs-lookup"><span data-stu-id="ed4af-110">D</span></span>     | <span data-ttu-id="ed4af-111">Désactivez la restauration et continuez sans demander à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed4af-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="ed4af-112">F</span><span class="sxs-lookup"><span data-stu-id="ed4af-112">F</span></span>     | <span data-ttu-id="ed4af-113">Échoue avec l’invite d’erreur d’espace disque insuffisant.</span><span class="sxs-lookup"><span data-stu-id="ed4af-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="ed4af-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ed4af-114">Remarks</span></span>

<span data-ttu-id="ed4af-115">Lorsque l’interface utilisateur est exécutée au niveau de base ou pas de l’interface utilisateur, le programme d’installation gère automatiquement la logique d’espace disque insuffisant.</span><span class="sxs-lookup"><span data-stu-id="ed4af-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="ed4af-116">Lorsque l’interface utilisateur s’exécute au niveau complet, des options supplémentaires peuvent être fournies à l’utilisateur, telles que l’invite avant de procéder à une restauration, la désactivation de la restauration ou la poursuite sans restauration lorsque le disque est plein.</span><span class="sxs-lookup"><span data-stu-id="ed4af-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="ed4af-117">Il revient au développeur du package de créer la séquence de la boîte de dialogue pour fournir les choix appropriés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed4af-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="ed4af-118">Les éléments disponibles sont les [EnableRollback ControlEvent,](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) Property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) Property et **PROMPTROLLBACKCOST** Property.</span><span class="sxs-lookup"><span data-stu-id="ed4af-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4af-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed4af-119">Requirements</span></span>



| <span data-ttu-id="ed4af-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed4af-120">Requirement</span></span> | <span data-ttu-id="ed4af-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed4af-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4af-122">Version</span><span class="sxs-lookup"><span data-stu-id="ed4af-122">Version</span></span><br/> | <span data-ttu-id="ed4af-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed4af-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed4af-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed4af-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed4af-125">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed4af-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ed4af-126">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4af-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed4af-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed4af-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4af-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed4af-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




