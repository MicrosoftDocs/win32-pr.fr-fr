---
description: Évolution de la prise en charge MUI sur les versions de Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Évolution de la prise en charge MUI sur les versions de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539105"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="696e4-103">Évolution de la prise en charge MUI sur les versions de Windows</span><span class="sxs-lookup"><span data-stu-id="696e4-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="696e4-104">Avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="696e4-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="696e4-105">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="696e4-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="696e4-106">Un système d’exploitation indépendant de la langue/MUI</span><span class="sxs-lookup"><span data-stu-id="696e4-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="696e4-107">Les scénarios de déploiement sont entièrement basés sur MUI</span><span class="sxs-lookup"><span data-stu-id="696e4-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="696e4-108">Déploiement d’une seule image</span><span class="sxs-lookup"><span data-stu-id="696e4-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="696e4-109">Amélioration du modèle de service</span><span class="sxs-lookup"><span data-stu-id="696e4-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="696e4-110">Infrastructure MUI</span><span class="sxs-lookup"><span data-stu-id="696e4-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="696e4-111">Gestion des langues</span><span class="sxs-lookup"><span data-stu-id="696e4-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="696e4-112">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="696e4-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="696e4-113">Avant Windows Vista</span><span class="sxs-lookup"><span data-stu-id="696e4-113">Before Windows Vista</span></span>

<span data-ttu-id="696e4-114">Avant la sortie de Windows Vista, Windows était fourni avec des images unilingues, ce qui signifiait que chaque version localisée de Windows contenait une seule langue pour son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="696e4-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="696e4-115">MUI était un module complémentaire de la version anglaise du système d’exploitation, et les packs de l’interface utilisateur multilingue pouvaient uniquement être ajoutés à certaines versions anglaises de Windows.</span><span class="sxs-lookup"><span data-stu-id="696e4-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="696e4-116">En cas d’installation sur la version anglaise de Windows, l’interface MUI permettait de modifier la langue de l’interface utilisateur du système d’exploitation en fonction des préférences des utilisateurs individuels dans l’une des langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="696e4-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="696e4-117">Le modèle MUI Pack n’a pas pu exposer la prise en charge MUI pour les applications.</span><span class="sxs-lookup"><span data-stu-id="696e4-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="696e4-118">Bien que les développeurs puissent créer des applications multilingues, ils devaient créer leurs propres mécanismes pour le faire.</span><span class="sxs-lookup"><span data-stu-id="696e4-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="696e4-119">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="696e4-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="696e4-120">Avec Windows Vista, Microsoft a fait un investissement significatif dans MUI.</span><span class="sxs-lookup"><span data-stu-id="696e4-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="696e4-121">Windows Vista est entièrement basé sur une plateforme MUI.</span><span class="sxs-lookup"><span data-stu-id="696e4-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="696e4-122">Bien que cela représente une avancée majeure dans la stratégie de localisation Windows, car il s’agit d’un activateur clé permettant à Microsoft d’offrir à Windows un plus grand nombre de langues qu’auparavant, il est tout d’abord un grand progrès pour les utilisateurs et les clients Windows.</span><span class="sxs-lookup"><span data-stu-id="696e4-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="696e4-123">Un système d’exploitation indépendant de la langue/MUI</span><span class="sxs-lookup"><span data-stu-id="696e4-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="696e4-124">La grande majorité des binaires de Windows Vista sont compatibles avec MUI et leurs données localisables sont stockées séparément du code.</span><span class="sxs-lookup"><span data-stu-id="696e4-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="696e4-125">Cela offre une certaine flexibilité, car différentes données de langage peuvent être ajoutées à tout moment.</span><span class="sxs-lookup"><span data-stu-id="696e4-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="696e4-126">Les scénarios de déploiement sont entièrement basés sur MUI</span><span class="sxs-lookup"><span data-stu-id="696e4-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="696e4-127">La conception de l’empaquetage et de l’installation de Windows Vista est basée sur MUI et toutes les données localisables sont empaquetées dans des packs spécifiques à la langue, et chaque module linguistique peut être déployé dans différents scénarios.</span><span class="sxs-lookup"><span data-stu-id="696e4-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="696e4-128">Par exemple, bien que les DVD de la version commerciale pour Windows Vista contiennent des versions en une seule langue, les utilisateurs de l’édition Ultimate peuvent télécharger des modules linguistiques MUI supplémentaires et basculer la langue de l’interface utilisateur à partir des **Options régionales et linguistiques** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="696e4-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="696e4-129">Les licences Enterprise Edition permettent d’accéder à toutes les langues et de les déployer.</span><span class="sxs-lookup"><span data-stu-id="696e4-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="696e4-130">Déploiement d’une seule image</span><span class="sxs-lookup"><span data-stu-id="696e4-130">Single image deployment</span></span>

<span data-ttu-id="696e4-131">Les clients d’entreprise et les fabricants d’ordinateurs OEM peuvent désormais réduire le nombre d’images dont ils ont besoin pour déployer Windows et des applications sur des ordinateurs de différents paramètres régionaux par le biais d’un déploiement d’image unique.</span><span class="sxs-lookup"><span data-stu-id="696e4-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="696e4-132">Avec MUI sur Windows Vista, une image contenant plusieurs langues peut être déployée sur n’importe quel utilisateur de langage, et les utilisateurs peuvent déterminer leurs propres langues préférées (dans la stratégie) au cours de l’installation ou de la première utilisation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="696e4-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="696e4-133">En particulier, les fabricants d’ordinateurs OEM peuvent placer de nombreux langages d’interface utilisateur sur leurs nouveaux ordinateurs pour permettre aux utilisateurs d’en sélectionner un à partir du centre d’accueil.</span><span class="sxs-lookup"><span data-stu-id="696e4-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="696e4-134">Ainsi, à partir d’une image avec plusieurs modules linguistiques, le programme d’installation affiche une liste des langues disponibles et permet aux utilisateurs de choisir l’un d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="696e4-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="696e4-135">Tous les paramètres internationaux sont ensuite définis pour correspondre à la langue ou aux paramètres régionaux sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="696e4-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="696e4-136">Amélioration du modèle de service</span><span class="sxs-lookup"><span data-stu-id="696e4-136">Improved servicing model</span></span>

<span data-ttu-id="696e4-137">Le même package QFE ou correctif de sécurité peut désormais être installé sur tous les systèmes de langue.</span><span class="sxs-lookup"><span data-stu-id="696e4-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="696e4-138">Cela est essentiel, car il permet une plus grande rapidité des correctifs de sécurité et permet à tous les utilisateurs internationaux de tirer parti de la même durée de disponibilité de tous les correctifs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="696e4-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="696e4-139">Infrastructure MUI</span><span class="sxs-lookup"><span data-stu-id="696e4-139">MUI infrastructure</span></span>

<span data-ttu-id="696e4-140">À compter de Windows Vista, les API MUI sont disponibles pour permettre aux développeurs de tirer parti des mécanismes MUI pour leurs propres applications, sans avoir à créer une logique personnalisée pour la gestion des ressources et la gestion des langues.</span><span class="sxs-lookup"><span data-stu-id="696e4-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="696e4-141">Gestion des langues</span><span class="sxs-lookup"><span data-stu-id="696e4-141">Language management</span></span>

<span data-ttu-id="696e4-142">Les API MUI de base qui fournissent des fonctionnalités de gestion de la langue de l’interface utilisateur sont disponibles dans le cadre de l’infrastructure MUI.</span><span class="sxs-lookup"><span data-stu-id="696e4-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="696e4-143">Pour faciliter la gestion des différents paramètres de langue de l’interface utilisateur au niveau du système, de l’utilisateur et de l’application, MUI les combine en interne dans une liste hiérarchisée unique.</span><span class="sxs-lookup"><span data-stu-id="696e4-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="696e4-144">MUI implémente ensuite un mécanisme de secours basé sur cette liste hiérarchisée, ce qui permet d’utiliser des solutions de localisation partielles tout en fournissant aux utilisateurs une expérience de langue d’interface utilisateur appropriée, si elle n’est pas préférée.</span><span class="sxs-lookup"><span data-stu-id="696e4-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="696e4-145">Par exemple, un système exécutant la version espagnole de Windows Vista avec un pack linguistique LIP (Language Interface Pack) catalan installé sur le système d’exploitation de base peut prendre en charge le comportement suivant : le système essaiera d’abord d’afficher ses ressources en catalan et, si ces ressources ne sont pas disponibles en catalan, fournissez à l’utilisateur des ressources espagnoles à la place.</span><span class="sxs-lookup"><span data-stu-id="696e4-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="696e4-146">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="696e4-146">Resource handling</span></span>

<span data-ttu-id="696e4-147">Avec l’infrastructure MUI améliorée qui est disponible à partir de Windows Vista, la plupart des technologies de ressources courantes sont compatibles avec l’interface MUI.</span><span class="sxs-lookup"><span data-stu-id="696e4-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="696e4-148">Le tableau suivant fournit des informations supplémentaires sur la prise en charge de la gestion des ressources disponibles dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="696e4-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="696e4-149">Category</span><span class="sxs-lookup"><span data-stu-id="696e4-149">Category</span></span></th>
<th><span data-ttu-id="696e4-150">Support</span><span class="sxs-lookup"><span data-stu-id="696e4-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="696e4-151">Types de ressources pris en charge</span><span class="sxs-lookup"><span data-stu-id="696e4-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="696e4-152">Ressource Win32/non managée :. DLL/. EXE/. OCX</span><span class="sxs-lookup"><span data-stu-id="696e4-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="696e4-153">Inscriptions liées à l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="696e4-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="696e4-154">Ressources liées à la gestion : journal des événements, fichiers de composant logiciel enfichable/MSC</span><span class="sxs-lookup"><span data-stu-id="696e4-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="696e4-155">WMI : MOF/MFL</span><span class="sxs-lookup"><span data-stu-id="696e4-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="696e4-156">Stratégie de groupe : ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="696e4-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="696e4-157">Resources.dll géré</span><span class="sxs-lookup"><span data-stu-id="696e4-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="696e4-158">Outils de développement</span><span class="sxs-lookup"><span data-stu-id="696e4-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="696e4-159">Pour Win32 : RC.exe, MUIRCT.exe et Visual Studio 2005 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="696e4-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="696e4-160">Prise en charge limitée des types de ressources</span><span class="sxs-lookup"><span data-stu-id="696e4-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="696e4-161">fichiers d’aide \*. chm</span><span class="sxs-lookup"><span data-stu-id="696e4-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



