---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-protection de l’exécution des données/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc73fcd70a244288aceaead426bf09f07656740d
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314772"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="7346a-103">Internet Explorer 8-protection de l’exécution des données/NX</span><span class="sxs-lookup"><span data-stu-id="7346a-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7346a-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="7346a-104">Affected Platforms</span></span>

 <span data-ttu-id="7346a-105">**Clients** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="7346a-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="7346a-106">**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7346a-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="7346a-107">Internet Explorer 8 activera la protection DEP/NX lorsqu’elle sera exécutée sur un système d’exploitation avec la dernière Service Pack.</span><span class="sxs-lookup"><span data-stu-id="7346a-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="7346a-108">Avec Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 et Windows Server 2008 tous les paramètres DEP/NX sont activés par défaut dans Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="7346a-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="7346a-109">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7346a-109">Feature Impact</span></span>

<span data-ttu-id="7346a-110">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="7346a-110">**Severity** - Medium</span></span>  
<span data-ttu-id="7346a-111">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="7346a-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="7346a-112">En règle générale, les applications qui s’exécutent dans Internet Explorer et qui ne sont pas compatibles avec DEP/NX se bloqueront au démarrage et ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="7346a-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="7346a-113">Internet Explorer peut se bloquer au démarrage si des modules complémentaires qui ne sont pas compatibles avec DEP/NX sont installés.</span><span class="sxs-lookup"><span data-stu-id="7346a-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="7346a-114">Description</span><span class="sxs-lookup"><span data-stu-id="7346a-114">Description</span></span>

<span data-ttu-id="7346a-115">DEP/NX est une fonctionnalité de sécurité qui permet d’atténuer les vulnérabilités liées à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7346a-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="7346a-116">À compter d’Internet Explorer 8, tous les processus Internet Explorer activent la fonctionnalité DEP/NX par défaut.</span><span class="sxs-lookup"><span data-stu-id="7346a-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="7346a-117">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="7346a-117">Manifestation of Impact</span></span>

<span data-ttu-id="7346a-118">Le noyau Windows surveille l’exécution d’un programme.</span><span class="sxs-lookup"><span data-stu-id="7346a-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="7346a-119">Si le noyau détecte une tentative d’exécution du code à partir d’une page de mémoire qui n’est pas marquée comme exécutable, le noyau interrompt l’exécution du programme, ce qui provoque un « incident ».</span><span class="sxs-lookup"><span data-stu-id="7346a-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="7346a-120">Il s’agit d’une mesure de sécurité qui permet de s’assurer que les vulnérabilités liées à la mémoire (par exemple, les débordements de mémoire tampon) de l’application ne peuvent pas être exploitées pour exécuter du code arbitraire.</span><span class="sxs-lookup"><span data-stu-id="7346a-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="7346a-121">Atténuation des End-User</span><span class="sxs-lookup"><span data-stu-id="7346a-121">End-User Mitigation</span></span>

-   <span data-ttu-id="7346a-122">Installez une version ultérieure du module complémentaire ou de l’infrastructure compatible avec DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7346a-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="7346a-123">Exécutez Internet Explorer avec élévation de privilèges en tant qu’administrateur, puis désactivez la case à cocher DEP/NX à l’aide de la case à cocher **activer la protection de la mémoire pour atténuer les attaques en ligne** sous l’onglet **options**  /  **avancées** d’Internet.</span><span class="sxs-lookup"><span data-stu-id="7346a-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="7346a-124">Solution de développeur</span><span class="sxs-lookup"><span data-stu-id="7346a-124">Developer Solution</span></span>

<span data-ttu-id="7346a-125">Compilez les applications à l’aide des dernières versions des frameworks compatibles avec DEP.</span><span class="sxs-lookup"><span data-stu-id="7346a-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="7346a-126">Exploitation des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7346a-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="7346a-127">Utiliser l’option de l’éditeur de liens/NXCOMPAT pour indiquer la compatibilité DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7346a-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="7346a-128">Choisir votre code dans d’autres défenses disponibles, telles que la protection de la pile (/GS), la gestion sécurisée des exceptions (/SafeSEH) et l’ASLR (/DynamicBase)</span><span class="sxs-lookup"><span data-stu-id="7346a-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="7346a-129">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="7346a-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="7346a-130">Testez votre code avec DEP/NX activé à l’aide de la dernière version publiée d’Internet Explorer sur Windows Vista SP1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7346a-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="7346a-131">Testez avec Internet Explorer 7 sur Windows Vista après l’activation de l’option DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7346a-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="7346a-132">Pour activer DEP/NX pour Internet Explorer 7, exécutez Internet Explorer en tant qu’administrateur, puis activez la case à cocher appropriée dans les outils > options Internet > onglet Avancé.</span><span class="sxs-lookup"><span data-stu-id="7346a-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="7346a-133">Exécutez l’outil de test de compatibilité d’Internet Explorer (IECTT), fourni avec Application Compatibility Toolkit (ACT) pour localiser les problèmes potentiels dus aux modifications DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7346a-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7346a-134">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="7346a-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="7346a-135">Sécurité d’Internet Explorer 8, partie I : protection de la mémoire DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7346a-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="7346a-136">Prévention de l’exécution des données</span><span class="sxs-lookup"><span data-stu-id="7346a-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="7346a-137">Nouvelles API NX ajoutées à Windows Vista SP1, Windows XP SP3 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7346a-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="7346a-138">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="7346a-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="7346a-139">[Problèmes connus liés aux fonctionnalités de sécurité d’Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="7346a-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
