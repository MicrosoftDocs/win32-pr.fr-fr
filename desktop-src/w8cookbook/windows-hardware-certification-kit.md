---
title: Kit de certification matérielle Windows
description: Kit de certification matérielle Windows
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031987"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="bc1af-103">Kit de certification matérielle Windows</span><span class="sxs-lookup"><span data-stu-id="bc1af-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="bc1af-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="bc1af-104">Platforms</span></span>

 <span data-ttu-id="bc1af-105">**Clients** -Windows 7 \| Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc1af-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="bc1af-106">**Serveurs** -windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc1af-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="bc1af-107">**Serveur/contrôleur** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc1af-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="bc1af-108">Description</span><span class="sxs-lookup"><span data-stu-id="bc1af-108">Description</span></span>

<span data-ttu-id="bc1af-109">Le kit de certification matérielle Windows permet aux développeurs, aux ISV, aux IHV et aux OEM de certifier leurs périphériques matériels, leurs systèmes et les pilotes de filtre pour les systèmes d’exploitation Windows les plus récents.</span><span class="sxs-lookup"><span data-stu-id="bc1af-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="bc1af-110">Il contient tous les outils et la documentation dont vous avez besoin pour certifier votre matériel et les pilotes de filtre pour les systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="bc1af-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="bc1af-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc1af-111">Windows 8</span></span>
-   <span data-ttu-id="bc1af-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc1af-112">Windows Server 2012</span></span>
-   <span data-ttu-id="bc1af-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bc1af-113">Windows 7</span></span>
-   <span data-ttu-id="bc1af-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bc1af-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="bc1af-115">Le kit de certification matérielle Windows remplace le kit de logo Windows et fait partie du programme de certification Windows.</span><span class="sxs-lookup"><span data-stu-id="bc1af-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="bc1af-116">Utilisation ou meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="bc1af-116">Usage or best practices</span></span>

<span data-ttu-id="bc1af-117">Avant de pouvoir tester le matériel ou le pilote de filtre, vous devez configurer l’environnement de test approprié en fonction du matériel ou du pilote de filtre que vous certifiez.</span><span class="sxs-lookup"><span data-stu-id="bc1af-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="bc1af-118">Cela comprend le contrôleur, le client et le matériel potentiellement supplémentaire (par exemple, les appareils multifonctions) ou les logiciels.</span><span class="sxs-lookup"><span data-stu-id="bc1af-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="bc1af-119">Une fois votre environnement configuré, vous pouvez tester votre matériel à l’aide de l’outil Studio de New TPM.</span><span class="sxs-lookup"><span data-stu-id="bc1af-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="bc1af-120">Ces étapes décrivent le processus de test de certification.</span><span class="sxs-lookup"><span data-stu-id="bc1af-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="bc1af-121">Configurer un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="bc1af-121">Set up test environment.</span></span>
2.  <span data-ttu-id="bc1af-122">Crée un projet.</span><span class="sxs-lookup"><span data-stu-id="bc1af-122">Create a project.</span></span>
3.  <span data-ttu-id="bc1af-123">Créez un ou plusieurs pools de machines.</span><span class="sxs-lookup"><span data-stu-id="bc1af-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="bc1af-124">Sélectionnez les fonctionnalités à valider.</span><span class="sxs-lookup"><span data-stu-id="bc1af-124">Select features to validate.</span></span>
5.  <span data-ttu-id="bc1af-125">Sélectionnez et exécutez des tests sur ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bc1af-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="bc1af-126">Afficher les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="bc1af-126">View test results.</span></span>
7.  <span data-ttu-id="bc1af-127">Soumettez votre package.</span><span class="sxs-lookup"><span data-stu-id="bc1af-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="bc1af-128">Ressources</span><span class="sxs-lookup"><span data-stu-id="bc1af-128">Resources</span></span>

-   [<span data-ttu-id="bc1af-129">Développement de matériel Windows</span><span class="sxs-lookup"><span data-stu-id="bc1af-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="bc1af-130">[Programme de certification matérielle Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc1af-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="bc1af-131">[Commencer à développer du matériel pour Windows](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="bc1af-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 