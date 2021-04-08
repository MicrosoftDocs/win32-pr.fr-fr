---
title: Logiciel anti-programme malveillant à lancement anticipé (ELAM)
description: Logiciel anti-programme malveillant à lancement anticipé (ELAM)
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104042898"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="5d845-103">Logiciel anti-programme malveillant à lancement anticipé (ELAM)</span><span class="sxs-lookup"><span data-stu-id="5d845-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="5d845-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="5d845-104">Platforms</span></span>

 <span data-ttu-id="5d845-105">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d845-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="5d845-106">**Serveurs** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d845-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="5d845-107">Description</span><span class="sxs-lookup"><span data-stu-id="5d845-107">Description</span></span>

<span data-ttu-id="5d845-108">Comme le logiciel anti-programme malveillant est devenu mieux et mieux adapté à la détection des programmes malveillants du runtime, les attaquants deviennent également mieux adaptés à la création de rootkits qui peuvent masquer la détection.</span><span class="sxs-lookup"><span data-stu-id="5d845-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="5d845-109">La détection de programmes malveillants qui démarrent tôt au cours du cycle de démarrage est un défi que la plupart des fournisseurs sont tenus de faire face à la diligence.</span><span class="sxs-lookup"><span data-stu-id="5d845-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="5d845-110">En règle générale, ils créent des piratages système qui ne sont pas pris en charge par le système d’exploitation hôte et qui peuvent entraîner le placement de l’ordinateur dans un état instable.</span><span class="sxs-lookup"><span data-stu-id="5d845-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="5d845-111">Jusqu’à présent, Windows n’a pas fourni un bon moyen de détecter et de résoudre ces menaces de démarrage anticipé.</span><span class="sxs-lookup"><span data-stu-id="5d845-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="5d845-112">Windows 8 introduit une nouvelle fonctionnalité appelée démarrage sécurisé, qui protège la configuration et les composants de démarrage de Windows et charge un pilote ELAM (anti-programme malveillant) à lancement anticipé.</span><span class="sxs-lookup"><span data-stu-id="5d845-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="5d845-113">Ce pilote démarre avant les autres pilotes de démarrage et permet l’évaluation de ces pilotes et aide le noyau Windows à déterminer s’ils doivent être initialisés.</span><span class="sxs-lookup"><span data-stu-id="5d845-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5d845-114">Manifestation</span><span class="sxs-lookup"><span data-stu-id="5d845-114">Manifestation</span></span>

<span data-ttu-id="5d845-115">En étant lancé en premier par le noyau, ELAM est assuré d’être lancé avant tout logiciel tiers. il est donc en mesure de détecter les logiciels malveillants dans le processus de démarrage et de les empêcher de s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="5d845-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="5d845-116">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="5d845-116">Mitigation</span></span>

<span data-ttu-id="5d845-117">Les pilotes de démarrage sont initialisés en fonction de la classification retournée par le pilote ELAM conformément à une stratégie d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="5d845-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="5d845-118">Par défaut, la stratégie initialise les pilotes connus et inconnus, mais n’initialise pas les pilotes incorrects connus.</span><span class="sxs-lookup"><span data-stu-id="5d845-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="5d845-119">Un administrateur système peut spécifier une stratégie personnalisée via stratégie de groupe qui peut empêcher des pilotes inconnus d’initialiser ou peut activer des pilotes qui sont critiques pour le processus de démarrage, mais qui ont été falsifiés, le démarrage doit être initialisé.</span><span class="sxs-lookup"><span data-stu-id="5d845-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="5d845-120">Solution</span><span class="sxs-lookup"><span data-stu-id="5d845-120">Solution</span></span>

<span data-ttu-id="5d845-121">Un pilote ELAM doit s’inscrire pour les rappels de noyau afin d’obtenir des informations sur chaque pilote de démarrage lors de son initialisation.</span><span class="sxs-lookup"><span data-stu-id="5d845-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="5d845-122">Le pilote ELAM peut ensuite retourner une classification pour chaque pilote.</span><span class="sxs-lookup"><span data-stu-id="5d845-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="5d845-123">Ces fonctions sont requises :</span><span class="sxs-lookup"><span data-stu-id="5d845-123">These functions are required:</span></span>

-   [<span data-ttu-id="5d845-124">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="5d845-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="5d845-125">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="5d845-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="5d845-126">Un pilote ELAM peut également s’inscrire pour les rappels du Registre.</span><span class="sxs-lookup"><span data-stu-id="5d845-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="5d845-127">Cela permet au pilote ELAM d’inspecter les données de configuration utilisées par chaque pilote de démarrage.</span><span class="sxs-lookup"><span data-stu-id="5d845-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="5d845-128">Le pilote ELAM peut ensuite bloquer ou modifier les données avant qu’elles ne soient utilisées par les pilotes de démarrage, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5d845-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="5d845-129">Ces fonctions sont requises :</span><span class="sxs-lookup"><span data-stu-id="5d845-129">These functions are required:</span></span>

-   [<span data-ttu-id="5d845-130">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="5d845-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="5d845-131">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="5d845-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="5d845-132">Pour plus d’informations sur la configuration requise pour le pilote ELAM et l’utilisation des API, consultez [lancement anticipé d’un logiciel anti-programme malveillant](/windows-hardware/drivers/install/early-launch-antimalware).</span><span class="sxs-lookup"><span data-stu-id="5d845-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="5d845-133">Tests</span><span class="sxs-lookup"><span data-stu-id="5d845-133">Tests</span></span>

<span data-ttu-id="5d845-134">Les pilotes ELAM doivent être spécialement signés par Microsoft pour s’assurer qu’ils sont démarrés par le noyau Windows au début du processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="5d845-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="5d845-135">Pour obtenir la signature, les pilotes ELAM doivent transmettre un ensemble de tests de certification pour vérifier les performances et d’autres comportements.</span><span class="sxs-lookup"><span data-stu-id="5d845-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="5d845-136">Ces tests sont inclus dans le kit de certification matérielle Windows.</span><span class="sxs-lookup"><span data-stu-id="5d845-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="5d845-137">Ressources</span><span class="sxs-lookup"><span data-stu-id="5d845-137">Resources</span></span>

-   [<span data-ttu-id="5d845-138">Logiciel anti-programme malveillant à lancement anticipé</span><span class="sxs-lookup"><span data-stu-id="5d845-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="5d845-139">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="5d845-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="5d845-140">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="5d845-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="5d845-141">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="5d845-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="5d845-142">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="5d845-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="5d845-143">Certification matérielle avec la présentation de la Conférence du kit de certification matérielle Windows</span><span class="sxs-lookup"><span data-stu-id="5d845-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="5d845-144">Télécharger les kits et les outils</span><span class="sxs-lookup"><span data-stu-id="5d845-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
