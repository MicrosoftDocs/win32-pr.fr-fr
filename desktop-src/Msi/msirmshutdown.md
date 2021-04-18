---
description: La propriété MSIRMSHUTDOWN détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés pour permettre l’installation de la mise à jour.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propriété MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526594"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="34054-103">Propriété MSIRMSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="34054-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="34054-104">La propriété **MSIRMSHUTDOWN** détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés pour permettre l’installation de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="34054-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="34054-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="34054-105">Value</span></span>



| <span data-ttu-id="34054-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="34054-106">Value</span></span>                                                                        | <span data-ttu-id="34054-107">Signification</span><span class="sxs-lookup"><span data-stu-id="34054-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34054-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="34054-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="34054-109">Les processus ou services qui utilisent actuellement des fichiers affectés par la mise à jour sont arrêtés.</span><span class="sxs-lookup"><span data-stu-id="34054-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="34054-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="34054-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="34054-111">Les processus ou services qui utilisent actuellement des fichiers affectés par la mise à jour et qui ne répondent pas au [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md)sont forcés à s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="34054-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="34054-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="34054-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="34054-113">Les processus ou services qui utilisent actuellement des fichiers affectés par la mise à jour sont arrêtés uniquement s’ils ont tous été inscrits pour un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="34054-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="34054-114">Si un processus ou un service n’a pas été inscrit pour un redémarrage, aucun processus ou service n’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="34054-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34054-115">Notes</span><span class="sxs-lookup"><span data-stu-id="34054-115">Remarks</span></span>

<span data-ttu-id="34054-116">La propriété **MSIRMSHUTDOWN** est ignorée si le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’est pas disponible ou est désactivé.</span><span class="sxs-lookup"><span data-stu-id="34054-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="34054-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34054-117">Requirements</span></span>



| <span data-ttu-id="34054-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34054-118">Requirement</span></span> | <span data-ttu-id="34054-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="34054-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34054-120">Version</span><span class="sxs-lookup"><span data-stu-id="34054-120">Version</span></span><br/> | <span data-ttu-id="34054-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34054-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34054-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34054-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34054-123">Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="34054-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34054-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34054-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34054-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="34054-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="34054-126">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="34054-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
