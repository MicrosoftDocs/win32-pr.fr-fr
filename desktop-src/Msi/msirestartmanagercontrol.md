---
description: La propriété MSIRESTARTMANAGERCONTROL spécifie si le package Windows Installer utilise les fonctionnalités du gestionnaire de redémarrage ou de la boîte de dialogue FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propriété MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537601"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="09a48-103">Propriété MSIRESTARTMANAGERCONTROL</span><span class="sxs-lookup"><span data-stu-id="09a48-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="09a48-104">La propriété **MSIRESTARTMANAGERCONTROL** spécifie si le package Windows Installer utilise les fonctionnalités du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) ou de la [boîte de dialogue FilesInUse](filesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="09a48-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="09a48-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="09a48-105">Value</span></span>



| <span data-ttu-id="09a48-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="09a48-106">Value</span></span>                                                                                        | <span data-ttu-id="09a48-107">Signification</span><span class="sxs-lookup"><span data-stu-id="09a48-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09a48-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="09a48-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="09a48-109">Il s’agit de la valeur par défaut si la propriété n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="09a48-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="09a48-110">Windows Installer tente toujours d’utiliser le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09a48-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="09a48-111"><dt>Désactive</dt></span><span class="sxs-lookup"><span data-stu-id="09a48-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="09a48-112">Désactive l’interaction du package avec le gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md).</span><span class="sxs-lookup"><span data-stu-id="09a48-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="09a48-113">Windows Installer utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="09a48-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="09a48-114"><dt>"DisableShutdown"</dt></span><span class="sxs-lookup"><span data-stu-id="09a48-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="09a48-115">Windows Installer utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="09a48-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="09a48-116">Ce paramètre désactive les tentatives du gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md) afin d’atténuer les redémarrages lors de l’installation d’un Windows Installer Package qui n’a pas été créé pour utiliser le gestionnaire de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="09a48-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="09a48-117">Le programme d’installation utilise toujours le gestionnaire de redémarrage pour détecter les fichiers utilisés par les applications.</span><span class="sxs-lookup"><span data-stu-id="09a48-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="09a48-118">Notes</span><span class="sxs-lookup"><span data-stu-id="09a48-118">Remarks</span></span>

<span data-ttu-id="09a48-119">La propriété **MSIRESTARTMANAGERCONTROL** est ignorée si le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’est pas disponible ou est désactivé.</span><span class="sxs-lookup"><span data-stu-id="09a48-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="09a48-120">La valeur de cette propriété peut être modifiée à l’aide de transformations ou de mises à niveau de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="09a48-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="09a48-121">La modification de la valeur de cette propriété à partir d’actions personnalisées n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="09a48-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a48-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09a48-122">Requirements</span></span>



| <span data-ttu-id="09a48-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09a48-123">Requirement</span></span> | <span data-ttu-id="09a48-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="09a48-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a48-125">Version</span><span class="sxs-lookup"><span data-stu-id="09a48-125">Version</span></span><br/> | <span data-ttu-id="09a48-126">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="09a48-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="09a48-127">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09a48-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="09a48-128">Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="09a48-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09a48-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09a48-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a48-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="09a48-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="09a48-131">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="09a48-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="09a48-132">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="09a48-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
