---
title: Services de déploiement Windows
description: Déployez des systèmes d’exploitation Windows. Configurez de nouveaux clients avec une installation réseau sans obliger les administrateurs à visiter chaque ordinateur ou à installer directement à partir d’un CD ou d’un DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Services de déploiement Windows (services de déploiement Windows)
- Services de déploiement Windows Services de déploiement Windows, page d’hébergement
- services de déploiement Windows Deployment Services
- Services de déploiement Windows WDS voir services de déploiement Windows
- Services d’installation à distance services de déploiement Windows Voir services de déploiement Windows
- Services de déploiement Windows RIS voir services de déploiement Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512525"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="c2b02-110">Services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="c2b02-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="c2b02-111">Objectif</span><span class="sxs-lookup"><span data-stu-id="c2b02-111">Purpose</span></span>

<span data-ttu-id="c2b02-112">Les services de déploiement Windows (WDS) sont la version révisée des services d’installation à distance (RIS).</span><span class="sxs-lookup"><span data-stu-id="c2b02-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="c2b02-113">WDS permet le déploiement de systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="c2b02-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="c2b02-114">Vous pouvez utiliser WDS pour configurer de nouveaux clients avec une installation réseau sans obliger les administrateurs à visiter chaque ordinateur ou à installer directement à partir d’un CD ou d’un DVD.</span><span class="sxs-lookup"><span data-stu-id="c2b02-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c2b02-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="c2b02-115">Developer audience</span></span>

<span data-ttu-id="c2b02-116">L’audience principale du développeur de l’API WDS concerne les groupes qui développent des outils et des processus personnalisés pour l’informatique et d’autres groupes d’administration de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c2b02-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="c2b02-117">Dans les environnements où la solution standard des services de déploiement Windows (WDS) ne peut pas être utilisée, l’API WDS autorise l’accès par programmation à certains composants de WDS.</span><span class="sxs-lookup"><span data-stu-id="c2b02-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="c2b02-118">Les fabricants OEM (Original Equipment Manufacturers), les intégrateurs de systèmes et les professionnels de l’informatique d’entreprise qui recherchent des informations sur le déploiement de Windows sur de nouveaux ordinateurs doivent voir les informations relatives à la solution Windows Deployment Services (WDS) standard dans le [Guide pas à pas de la mise à jour des services de déploiement Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) et le [Kit d’installation automatisée (Windows AIK) (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span><span class="sxs-lookup"><span data-stu-id="c2b02-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c2b02-119">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="c2b02-119">Run-time requirements</span></span>

<span data-ttu-id="c2b02-120">WDS est disponible en tant que module complémentaire pour Windows Server 2003 avec Service Pack 1 (SP1) et est inclus dans le système d’exploitation à partir de Windows Server 2003 avec Service Pack 2 (SP2) et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c2b02-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="c2b02-121">L’API du serveur PXE WDS requiert que le rôle serveur WDS sur le serveur implémente des fournisseurs PXE personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c2b02-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="c2b02-122">L’API cliente WDS requiert la phase de traitement de l’installation de Microsoft environnement de préinstallation Windows (WinPE) (Windows PE 2,0).</span><span class="sxs-lookup"><span data-stu-id="c2b02-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="c2b02-123">Une image de démarrage RAMDISK de Windows PE 2,0 dans le. Le format WIM doit être téléchargé dans le cadre du processus de démarrage réseau pour implémenter des clients WDS personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c2b02-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c2b02-124">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c2b02-124">In this section</span></span>



| <span data-ttu-id="c2b02-125">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c2b02-125">Topic</span></span>                                                                                                 | <span data-ttu-id="c2b02-126">Description</span><span class="sxs-lookup"><span data-stu-id="c2b02-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="c2b02-127">À propos de l’API des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="c2b02-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="c2b02-128">Informations générales sur l’API du serveur WDS et l’API client WDS.</span><span class="sxs-lookup"><span data-stu-id="c2b02-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="c2b02-129">Informations de référence sur les services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="c2b02-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="c2b02-130">Décrit les fonctions et les structures des services de déploiement Windows.</span><span class="sxs-lookup"><span data-stu-id="c2b02-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

