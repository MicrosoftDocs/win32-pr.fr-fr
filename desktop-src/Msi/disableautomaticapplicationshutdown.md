---
description: Si cette stratégie système par ordinateur est définie sur 1 (un), Windows Installer n’interagit pas avec le gestionnaire de redémarrage, mais elle utilisera la boîte de dialogue FilesInUse. Si cette stratégie système par ordinateur est définie sur 2 (deux), Windows Installer utilise la boîte de dialogue FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519637"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="14a58-103">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="14a58-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="14a58-104">Si cette stratégie système par ordinateur est définie sur 1 (un), Windows Installer n’interagit pas avec le [Gestionnaire de redémarrage](/windows/desktop/RstMgr/restart-manager-portal), mais elle utilisera la [boîte de dialogue FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="14a58-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="14a58-105">Si cette stratégie système par ordinateur est définie sur 2 (deux), Windows Installer utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="14a58-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="14a58-106">Ce paramètre désactive les tentatives du gestionnaire de [redémarrage](/windows/desktop/RstMgr/restart-manager-portal) afin d’atténuer les redémarrages lors de l’installation d’un Windows Installer Package qui n’a pas été créé pour utiliser le gestionnaire de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="14a58-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="14a58-107">Le programme d’installation utilise toujours le gestionnaire de redémarrage pour détecter les fichiers utilisés par les applications.</span><span class="sxs-lookup"><span data-stu-id="14a58-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="14a58-108">La stratégie DisableAutomaticApplicationShutdown est disponible à partir de Windows Installer version 4,0 sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="14a58-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="14a58-109">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="14a58-109">Registry Key</span></span>

<span data-ttu-id="14a58-110">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="14a58-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="14a58-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="14a58-111">Data Type</span></span>

<span data-ttu-id="14a58-112">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="14a58-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="14a58-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14a58-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a58-114">**MSIRESTARTMANAGERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="14a58-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="14a58-115">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="14a58-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
