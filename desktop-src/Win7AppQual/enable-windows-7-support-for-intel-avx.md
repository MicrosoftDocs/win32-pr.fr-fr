---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Activer la prise en charge de Windows 7 pour Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530254"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="75c34-103">Activer la prise en charge de Windows 7 pour Intel AVX</span><span class="sxs-lookup"><span data-stu-id="75c34-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="75c34-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="75c34-104">Affected Platforms</span></span>

 <span data-ttu-id="75c34-105">**Clients** -Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="75c34-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="75c34-106">**Serveurs** -Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="75c34-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="75c34-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="75c34-107">Feature Impact</span></span>

 <span data-ttu-id="75c34-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="75c34-108">**Severity** - Low</span></span>  
<span data-ttu-id="75c34-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="75c34-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="75c34-110">Description</span><span class="sxs-lookup"><span data-stu-id="75c34-110">Description</span></span>

<span data-ttu-id="75c34-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="75c34-111">Intel<sup>?</sup></span></span> <span data-ttu-id="75c34-112">AVX (Advanced Vector Extensions)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="75c34-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="75c34-113">est une extension de type vectoriel à virgule flottante 256 bits SIMD de l’architecture Intel.</span><span class="sxs-lookup"><span data-stu-id="75c34-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="75c34-114">Il comprend des extensions pour les instructions et les ensembles d’registres.</span><span class="sxs-lookup"><span data-stu-id="75c34-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="75c34-115">Microsoft a développé des améliorations de l’API, telles que les fonctions XState, qui permettent aux applications d’accéder aux fonctionnalités et à l’état du processeur étendu et de les manipuler, y compris AVX.</span><span class="sxs-lookup"><span data-stu-id="75c34-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="75c34-116">Scénarios d’utilisation</span><span class="sxs-lookup"><span data-stu-id="75c34-116">Usage Scenarios</span></span>

<span data-ttu-id="75c34-117">Il existe trois niveaux généraux d’impact potentiel.</span><span class="sxs-lookup"><span data-stu-id="75c34-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="75c34-118">**Niveau 1 :** Les applications qui n’utilisent pas directement Intel AVX ne verront aucun impact sur leurs fonctionnalités, même si elles appellent des bibliothèques ou utilisent des compilateurs qui utilisent ou génèrent indirectement des extensions Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="75c34-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="75c34-119">Cela représente de loin la majorité des applications.</span><span class="sxs-lookup"><span data-stu-id="75c34-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="75c34-120">**Niveau 2 :** Les applications avancées qui utilisent explicitement le jeu d’instructions Intel AVX pourront accéder et modifier le contenu du Registre AVX lorsqu’une exception matérielle est générée.</span><span class="sxs-lookup"><span data-stu-id="75c34-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="75c34-121">Un très petit nombre d’applications se trouve dans cette catégorie, car cela implique une connaissance approfondie du flux d’instructions s’exécutant au moment de l’exception, par exemple les applications avec des sections écrites en langage assembleur ou celles qui génèrent du code machine au moment de l’exécution (par exemple, les runtimes de code managé avec compilation juste-à-temps).</span><span class="sxs-lookup"><span data-stu-id="75c34-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="75c34-122">**Niveau 3 :** Les applications du débogueur pourront accéder et manipuler l’État AVX dans l’application en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="75c34-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="75c34-123">Comment tirer parti des fonctionnalités de fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="75c34-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="75c34-124">**Niveau 1 :** Aucune action n’est nécessaire pour que les applications utilisent Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="75c34-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="75c34-125">**Niveau 2 :** Les applications de cette catégorie peuvent accéder et manipuler l’État AVX au moment de l’exception à partir de leurs filtres d’exception.</span><span class="sxs-lookup"><span data-stu-id="75c34-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="75c34-126">Après avoir obtenu le contexte du processeur de base via GetExceptionInformation, les filtres doivent :</span><span class="sxs-lookup"><span data-stu-id="75c34-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="75c34-127">**1.** Vérifiez la valeur de l' **indicateur \_ XSTATE du contexte** .</span><span class="sxs-lookup"><span data-stu-id="75c34-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="75c34-128">Cet indicateur indique la présence d’au moins une fonctionnalité XState dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="75c34-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="75c34-129">**2.** dans ce cas, appelez **GetXStateFeaturesMask** et testez la valeur de l’indicateur **XSTATE \_ AVX** dans le masque retourné.</span><span class="sxs-lookup"><span data-stu-id="75c34-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="75c34-130">Cela indique la présence de l’État AVX dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="75c34-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="75c34-131">**3.** appelez **LocateXStateFeature** pour récupérer l’emplacement réel où l’État AVX est stocké.</span><span class="sxs-lookup"><span data-stu-id="75c34-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="75c34-132">**Niveau 3 :** Il n’est pas nécessaire de mettre à jour les applications existantes du débogueur, sauf si elles souhaitent accéder aux registres Intel AVX :</span><span class="sxs-lookup"><span data-stu-id="75c34-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="75c34-133">**1.** pour déterminer si AVX est activé, le débogueur doit utiliser :</span><span class="sxs-lookup"><span data-stu-id="75c34-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="75c34-134">GetEnabledXStateFeatures pour obtenir un masque des fonctionnalités XState activées sur les processeurs x86 ou x64 afin de déterminer quelles fonctionnalités sont présentes et activées sur le système avant d’utiliser une fonctionnalité de processeur XState ou de manipuler des contextes XState</span><span class="sxs-lookup"><span data-stu-id="75c34-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="75c34-135">**2.** si AVX est présent et que vous souhaitez récupérer et manipuler l’État AVX à partir de l’application en cours de débogage (par exemple, GetThreadContext et SetThreadContext), le débogueur doit utiliser :</span><span class="sxs-lookup"><span data-stu-id="75c34-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="75c34-136">Fonction InitializeContext pour initialiser une structure de contexte à l’intérieur d’une mémoire tampon avec la taille et l’alignement nécessaires</span><span class="sxs-lookup"><span data-stu-id="75c34-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="75c34-137">Fonction CopyContext pour copier une structure de contexte source (y compris les XState) sur une structure de contexte de destination initialisée</span><span class="sxs-lookup"><span data-stu-id="75c34-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="75c34-138">**3.** pour tester, définir et localiser l’État AVX dans un contexte de processeur, le débogueur doit utiliser :</span><span class="sxs-lookup"><span data-stu-id="75c34-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="75c34-139">LocateXStateFeature pour récupérer un pointeur vers l’état du processeur pour une fonctionnalité XState individuelle dans une structure de contexte</span><span class="sxs-lookup"><span data-stu-id="75c34-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="75c34-140">GetXStateFeaturesMask pour retourner le masque des fonctionnalités XState définies dans une structure de contexte</span><span class="sxs-lookup"><span data-stu-id="75c34-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="75c34-141">SetXStateFeaturesMask pour définir le masque des fonctionnalités XState définies dans une structure de contexte</span><span class="sxs-lookup"><span data-stu-id="75c34-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="75c34-142">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="75c34-142">Links to Other Resources</span></span>

-   <span data-ttu-id="75c34-143">Pour plus d’informations sur les fonctions XState dans le SDK Windows, consultez [débogage de fonctions](../debug/debugging-functions.md).</span><span class="sxs-lookup"><span data-stu-id="75c34-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="75c34-144">Pour obtenir une vue d’ensemble des instructions et des fonctionnalités d’Intel AVX, consultez [Intel AVX : nouvelles frontières dans améliorations des performances et efficacité énergétique](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="75c34-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
