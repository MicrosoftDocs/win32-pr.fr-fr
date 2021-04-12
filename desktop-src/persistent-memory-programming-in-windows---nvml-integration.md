---
description: La technologie mémoire persistante (PM) fournit un accès au niveau octet aux médias non volatiles tout en réduisant considérablement la latence du stockage ou de la récupération des données.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programmation de mémoire persistante dans l’intégration de Windows-NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210359"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="3d842-103">Programmation de mémoire persistante dans l’intégration de Windows-NVML</span><span class="sxs-lookup"><span data-stu-id="3d842-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="3d842-104">La technologie mémoire persistante (PM) fournit un accès au niveau octet aux médias non volatiles tout en réduisant considérablement la latence du stockage ou de la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="3d842-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="3d842-105">Il crée un nouveau niveau entre la mémoire du système et le stockage traditionnel.</span><span class="sxs-lookup"><span data-stu-id="3d842-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="3d842-106">Tout programme dépendant ou mis à l’échelle avec des écritures rapides sur un support permanent peut tirer parti de PM.</span><span class="sxs-lookup"><span data-stu-id="3d842-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="3d842-107">L’objectif de cet article est de montrer comment la bibliothèque mémoire non volatile (NVML) peut être intégrée dans un projet Visual Studio pour faciliter son utilisation.</span><span class="sxs-lookup"><span data-stu-id="3d842-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="3d842-108">La mémoire persistante est parfois également appelée mémoire de classe de stockage (SCM).</span><span class="sxs-lookup"><span data-stu-id="3d842-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="3d842-109">PM et NVML</span><span class="sxs-lookup"><span data-stu-id="3d842-109">PM and NVML</span></span>

<span data-ttu-id="3d842-110">La première prise en charge de la mémoire persistante a été introduite dans Windows Server 2016 et la mise à jour anniversaire de Windows 10 (1607).</span><span class="sxs-lookup"><span data-stu-id="3d842-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="3d842-111">Pour une vue d’ensemble rapide, consultez ces deux vidéos channel9 :</span><span class="sxs-lookup"><span data-stu-id="3d842-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   [<span data-ttu-id="3d842-112">Utilisation de la mémoire non volatile (NVDIMM-N) comme stockage de bloc dans Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3d842-112">Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P466)
-   [<span data-ttu-id="3d842-113">Utilisation de la mémoire non volatile (NVDIMM-N) en tant que stockage Byte-Addressable dans Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3d842-113">Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P470)

<span data-ttu-id="3d842-114">Pour aider les développeurs à tirer parti des avantages offerts par la mémoire persistante, Microsoft a également contribué à mettre en œuvre la bibliothèque mémoire non volatile (NVML) dans Windows.</span><span class="sxs-lookup"><span data-stu-id="3d842-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="3d842-115">Cette bibliothèque fournit différents outils pour rendre les applications compatibles avec la mémoire persistante.</span><span class="sxs-lookup"><span data-stu-id="3d842-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="3d842-116">Par exemple, il contient du code qui vous permet de créer facilement un magasin clé-valeur prenant en charge les bases de code pour des recherches et des magasins extrêmement rapides.</span><span class="sxs-lookup"><span data-stu-id="3d842-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="3d842-117">Vous trouverez plus d’informations sur NVML, y compris des exemples, à la [bibliothèque NVM](https://pmem.io/nvml/).</span><span class="sxs-lookup"><span data-stu-id="3d842-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="3d842-118">Intégration de NVML dans un projet Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3d842-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="3d842-119">Télécharger les fichiers et en-têtes de la bibliothèque NVML</span><span class="sxs-lookup"><span data-stu-id="3d842-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="3d842-120">NVML est conservé sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="3d842-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="3d842-121">Vous pouvez compiler la source vous-même ou simplement télécharger des binaires compilés directement à partir de cet emplacement : [NVML Version 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span><span class="sxs-lookup"><span data-stu-id="3d842-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="3d842-122">Placez les fichiers et en-têtes de la bibliothèque dans le répertoire de votre choix, par exemple : « C : \\ NVML \\ lib » et « c : \\ NVML \\ Inc », respectivement.</span><span class="sxs-lookup"><span data-stu-id="3d842-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="3d842-123">Configurez votre projet comme suit :</span><span class="sxs-lookup"><span data-stu-id="3d842-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="3d842-124">Ouvrez votre projet Visual Studio et dans le « Explorateur de solutions », cliquez avec le bouton droit sur le nom de votre projet.</span><span class="sxs-lookup"><span data-stu-id="3d842-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="3d842-125">Ouvrez le volet des paramètres du projet en bas de la fenêtre contextuelle résultante.</span><span class="sxs-lookup"><span data-stu-id="3d842-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="3d842-126">Accédez à « propriétés de configuration-> C/C++ » et ajoutez le dossier dans lequel vous avez stocké l’en-tête (C : \\ NVML \\ Inc) dans le champ « autres répertoires Include ».</span><span class="sxs-lookup"><span data-stu-id="3d842-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="3d842-127">Ensuite, accédez à « propriétés de configuration-éditeur de liens > » et ajoutez le dossier dans lequel vous avez stocké la bibliothèque (C : \\ NVML \\ lib) dans le champ « répertoires de bibliothèques supplémentaires ».</span><span class="sxs-lookup"><span data-stu-id="3d842-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="3d842-128">Ensuite, assurez-vous que vous ciblez le projet pour la mise à jour anniversaire de Windows Server 2016 ou Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="3d842-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="3d842-129">Accédez à « propriétés de configuration-> général » et définissez le champ « version de la plateforme cible » sur « 10.0.14393.0 » et</span><span class="sxs-lookup"><span data-stu-id="3d842-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="3d842-130">Accédez à « propriétés de configuration-> C/C++ » et ajoutez « NTDDI \_ version = NTDDI \_ WIN10 \_ RS1 ; » au champ « préprocesseur ».</span><span class="sxs-lookup"><span data-stu-id="3d842-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="3d842-131">Inclure les en-têtes dans votre code et créer un lien vers les bibliothèques requises</span><span class="sxs-lookup"><span data-stu-id="3d842-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="3d842-132">À ce stade, vous pouvez simplement inclure les fichiers d’en-tête que vous souhaitez utiliser dans votre code comme n’importe quel autre fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="3d842-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="3d842-133">Par exemple, pour utiliser libpmem :</span><span class="sxs-lookup"><span data-stu-id="3d842-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="3d842-134">Ajoutez « \# include <libpmem. h> » et</span><span class="sxs-lookup"><span data-stu-id="3d842-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="3d842-135">Ajoutez « libpmem. lib » à « propriétés de configuration-éditeur de liens-> > d’entrée-> dépendances supplémentaires »</span><span class="sxs-lookup"><span data-stu-id="3d842-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="3d842-136">À ce stade, vous êtes prêt à appeler les fonctions de la bibliothèque directement dans votre code et à en tirer parti.</span><span class="sxs-lookup"><span data-stu-id="3d842-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



