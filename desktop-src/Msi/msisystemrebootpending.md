---
description: Le programme d’installation définit la valeur de la propriété MsiSystemRebootPending sur 1 s’il existe une opération en attente pour renommer un fichier.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propriété MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526362"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="66239-103">Propriété MsiSystemRebootPending</span><span class="sxs-lookup"><span data-stu-id="66239-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="66239-104">Le programme d’installation définit la valeur de la propriété **MsiSystemRebootPending** sur 1 s’il existe une opération en attente pour renommer un fichier.</span><span class="sxs-lookup"><span data-stu-id="66239-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="66239-105">Les auteurs de package peuvent baser une condition dans la [table LaunchCondition](launchcondition-table.md) sur cette propriété pour empêcher l’installation de leur package dans les cas où une opération est en attente pour renommer un fichier.</span><span class="sxs-lookup"><span data-stu-id="66239-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="66239-106">Cela peut être fait pour empêcher un redémarrage du système d’exploitation provoqué par le changement de nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="66239-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="66239-107">Le programme d’installation ne définit pas la propriété **MsiSystemRebootPending** dans tous les cas qui requièrent un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="66239-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="66239-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66239-108">Requirements</span></span>



| <span data-ttu-id="66239-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66239-109">Requirement</span></span> | <span data-ttu-id="66239-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="66239-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66239-111">Version</span><span class="sxs-lookup"><span data-stu-id="66239-111">Version</span></span><br/> | <span data-ttu-id="66239-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="66239-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="66239-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="66239-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="66239-114">Windows Installer 4,5 sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="66239-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="66239-115">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="66239-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66239-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66239-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66239-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66239-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="66239-118">Redémarrages du système</span><span class="sxs-lookup"><span data-stu-id="66239-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="66239-119">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="66239-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




