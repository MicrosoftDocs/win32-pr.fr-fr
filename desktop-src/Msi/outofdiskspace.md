---
description: Le programme d’installation définit la propriété OutOfDiskSpace sur TRUE si un volume qui est une cible de l’installation actuelle ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propriété OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525243"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="9a67b-103">Propriété OutOfDiskSpace</span><span class="sxs-lookup"><span data-stu-id="9a67b-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="9a67b-104">Le programme d’installation définit la propriété **OutOfDiskSpace** sur true si un volume qui est une cible de l’installation actuelle ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation.</span><span class="sxs-lookup"><span data-stu-id="9a67b-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="9a67b-105">Si tous les volumes disposent de suffisamment d’espace, la valeur est FALSe.</span><span class="sxs-lookup"><span data-stu-id="9a67b-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="9a67b-106">Les actions de résolution de sélection utilisent cette valeur pour annuler une installation et générer une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9a67b-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="9a67b-107">Cette propriété est valide à tout moment après l’exécution de l' [action CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9a67b-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="9a67b-108">L’état de la propriété [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) est mis à jour de manière dynamique chaque fois que le coût total d’installation est recalculé (par exemple, chaque fois que l’état d’installation d’une fonctionnalité est modifié via la boîte de dialogue de [sélection](selection-dialog.md) ).</span><span class="sxs-lookup"><span data-stu-id="9a67b-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a67b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9a67b-109">Remarks</span></span>

<span data-ttu-id="9a67b-110">Toute boîte de dialogue reposant sur la propriété **OutOfDiskSpace** pour déterminer s’il faut afficher une boîte de dialogue doit définir le [bit de style](trackdiskspace-dialog-style-bit.md) de la boîte de dialogue TrackDiskSpace pour la boîte de dialogue afin de mettre à jour dynamiquement l’espace sur les volumes cibles.</span><span class="sxs-lookup"><span data-stu-id="9a67b-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a67b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a67b-111">Requirements</span></span>



| <span data-ttu-id="9a67b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a67b-112">Requirement</span></span> | <span data-ttu-id="9a67b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a67b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a67b-114">Version</span><span class="sxs-lookup"><span data-stu-id="9a67b-114">Version</span></span><br/> | <span data-ttu-id="9a67b-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9a67b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9a67b-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a67b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9a67b-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a67b-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9a67b-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9a67b-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a67b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a67b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a67b-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9a67b-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




