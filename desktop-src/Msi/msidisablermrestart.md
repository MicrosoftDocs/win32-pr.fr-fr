---
description: La propriété MSIDISABLERMRESTART détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés et redémarrés pour permettre l’installation de la mise à jour.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propriété MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543216"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="14bb1-103">Propriété MSIDISABLERMRESTART</span><span class="sxs-lookup"><span data-stu-id="14bb1-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="14bb1-104">La propriété **MSIDISABLERMRESTART** détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés et redémarrés pour permettre l’installation de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="14bb1-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="14bb1-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="14bb1-105">Value</span></span>



| <span data-ttu-id="14bb1-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="14bb1-106">Value</span></span>                                                                        | <span data-ttu-id="14bb1-107">Signification</span><span class="sxs-lookup"><span data-stu-id="14bb1-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14bb1-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="14bb1-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="14bb1-109">Tous les services système qui ont été arrêtés pour installer la mise à jour sont redémarrés.</span><span class="sxs-lookup"><span data-stu-id="14bb1-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="14bb1-110">Toutes les applications qui se sont inscrites avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) sont redémarrées.</span><span class="sxs-lookup"><span data-stu-id="14bb1-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="14bb1-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="14bb1-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="14bb1-112">Les processus qui ont été arrêtés à l’aide du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pendant l’installation de la mise à jour ne sont pas redémarrés après l’application de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="14bb1-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="14bb1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="14bb1-113">Remarks</span></span>

<span data-ttu-id="14bb1-114">La propriété **MSIDISABLERMRESTART** est ignorée si le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’est pas disponible ou est désactivé.</span><span class="sxs-lookup"><span data-stu-id="14bb1-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="14bb1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14bb1-115">Requirements</span></span>



| <span data-ttu-id="14bb1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14bb1-116">Requirement</span></span> | <span data-ttu-id="14bb1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="14bb1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bb1-118">Version</span><span class="sxs-lookup"><span data-stu-id="14bb1-118">Version</span></span><br/> | <span data-ttu-id="14bb1-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="14bb1-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="14bb1-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="14bb1-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="14bb1-121">Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="14bb1-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14bb1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14bb1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bb1-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="14bb1-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="14bb1-124">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="14bb1-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
