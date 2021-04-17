---
description: Cette rubrique fournit une vue d’ensemble conceptuelle de la technologie MUI (Multilingual User Interface), la prise en charge de la plateforme qu’elle fournit pour l’activation de l’expérience utilisateur multilingue et les avantages qu’elle offre à l’écosystème Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Vue d’ensemble de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562704"
---
# <a name="overview-of-mui"></a><span data-ttu-id="f4318-103">Vue d’ensemble de MUI</span><span class="sxs-lookup"><span data-stu-id="f4318-103">Overview of MUI</span></span>

<span data-ttu-id="f4318-104">Cette rubrique fournit une vue d’ensemble conceptuelle de la technologie MUI (Multilingual User Interface), la prise en charge de la plateforme qu’elle fournit pour l’activation de l’expérience utilisateur multilingue et les avantages qu’elle offre à l’écosystème Windows.</span><span class="sxs-lookup"><span data-stu-id="f4318-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="f4318-105">Sur cette page :</span><span class="sxs-lookup"><span data-stu-id="f4318-105">On this page:</span></span>

-   [<span data-ttu-id="f4318-106">Besoin de l’informatique multilingue</span><span class="sxs-lookup"><span data-stu-id="f4318-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="f4318-107">Rôle de MUI dans l’activation de l’informatique multilingue</span><span class="sxs-lookup"><span data-stu-id="f4318-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="f4318-108">Concepts de base de MUI</span><span class="sxs-lookup"><span data-stu-id="f4318-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="f4318-109">Historique de MUI dans Windows</span><span class="sxs-lookup"><span data-stu-id="f4318-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="f4318-110">Avantages de la technologie MUI</span><span class="sxs-lookup"><span data-stu-id="f4318-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="f4318-111">Besoin de l’informatique multilingue</span><span class="sxs-lookup"><span data-stu-id="f4318-111">The need for multilingual computing</span></span>

<span data-ttu-id="f4318-112">Pour tirer parti des opportunités de croissance présentées par les marchés internationaux, les plateformes et les applications de Microsoft prennent en charge plus de langues, de cultures et de marchés que jamais.</span><span class="sxs-lookup"><span data-stu-id="f4318-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="f4318-113">La langue, la culture et les spécificités du marché sont toujours extrêmement pertinentes pour les utilisateurs internationaux, malgré l’amélioration des tendances de globalisation.</span><span class="sxs-lookup"><span data-stu-id="f4318-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="f4318-114">Le graphique à secteurs suivant montre que les orateurs non anglophones composent toujours 91,5% de la population mondiale.</span><span class="sxs-lookup"><span data-stu-id="f4318-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![graphique à secteurs avec trois segments ; l’une des « enceintes non anglaises 91,5% » est considérablement plus grande que les deux autres.](images/overview-of-mui-fig1.gif)

<span data-ttu-id="f4318-116">Dans le monde entier, il existe 193 pays et plus de 6 900 langues connues en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f4318-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="f4318-117">En anglais, en dépit de son rôle de langage professionnel, n’est parlé que de 8,5% du remplissage du monde en tant que premier ou deuxième langage.</span><span class="sxs-lookup"><span data-stu-id="f4318-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="f4318-118">Pour fournir des informations natives à 94% de la population mondiale, ces informations doivent être disponibles dans le 347 (environ 5%) des langues du monde qui ont au moins un million d’orateurs.</span><span class="sxs-lookup"><span data-stu-id="f4318-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="f4318-119">Cela est particulièrement vrai lorsque les tendances de globalisation ont augmenté les attentes de ces utilisateurs concernant la technologie et leur disponibilité sur leurs marchés.</span><span class="sxs-lookup"><span data-stu-id="f4318-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="f4318-120">Le besoin de localiser des logiciels dans un plus grand nombre de langues a augmenté au fil des années et Microsoft propose désormais Windows Vista et d’autres produits dans plus de langues que jamais.</span><span class="sxs-lookup"><span data-stu-id="f4318-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="f4318-121">Cette évolution est particulièrement claire avec Microsoft Windows, car elle est passée de la prise en charge de 30 langues avec Windows 98 à presque 100 avec Windows Vista, comme illustré dans le graphique à barres suivant.</span><span class="sxs-lookup"><span data-stu-id="f4318-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![graphique à barres indiquant que le nombre de langues est bien plus important dans Windows Vista que dans Windows 98 ou Windows XP](images/overview-of-mui-fig2.gif)

<span data-ttu-id="f4318-123">*Figure 2 : nombre de langues prises en charge par les versions de Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="f4318-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="f4318-124">Rôle de MUI dans l’activation de l’informatique multilingue</span><span class="sxs-lookup"><span data-stu-id="f4318-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="f4318-125">Comme nous l’avons vu dans la section précédente, la [globalisation](glossary-for-understanding-mui.md) et la [localisation](glossary-for-understanding-mui.md) des applications sont devenues une nécessité dans un monde plus intégré dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="f4318-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="f4318-126">En particulier, à mesure que de plus en plus d’entreprises sont en général, soit en interne, soit via leurs réseaux d’entreprise, la nécessité d’applications multilingues augmente considérablement.</span><span class="sxs-lookup"><span data-stu-id="f4318-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="f4318-127">Voici donc les obstacles auxquels ces sociétés sont confrontés pour le déploiement global de ces applications.</span><span class="sxs-lookup"><span data-stu-id="f4318-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="f4318-128">La prise en charge d’un plus grand nombre de langues pour les systèmes d’exploitation Windows, ainsi que d’applications logicielles conçues pour la plate-forme Windows, requiert de nouvelles stratégies qui permettent d’implémenter tous les principaux scénarios avec une surcharge d’ingénierie minimale.</span><span class="sxs-lookup"><span data-stu-id="f4318-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="f4318-129">La technologie MUI est destinée aux développeurs et aux éditeurs de logiciels indépendants visant à créer et à prendre en charge des applications multilingues pour la plate-forme Windows.</span><span class="sxs-lookup"><span data-stu-id="f4318-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="f4318-130">MUI est également très important pour les OEM et les entreprises, qui peuvent en tirer parti pour déployer le système d’exploitation Windows et ajouter des applications aux ordinateurs dans différentes langues via un déploiement d’image unique.</span><span class="sxs-lookup"><span data-stu-id="f4318-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="f4318-131">Concepts de base de MUI</span><span class="sxs-lookup"><span data-stu-id="f4318-131">Core concepts of MUI</span></span>

<span data-ttu-id="f4318-132">L’idée fondamentale de MUI est de [séparer le stockage des ressources localisables du code source](mui-fundamental-concepts-explained.md)de l’application, de façon à pouvoir concevoir une application multilingue comme une combinaison d’un binaire de base indépendant de la langue et d’un ensemble de fichiers de ressources localisés spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="f4318-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="f4318-133">Une fois que le code source de l’application est stocké séparément des ressources localisées, il devient facile de [charger dynamiquement les ressources localisées appropriées](mui-fundamental-concepts-explained.md) pour un contexte d’application donné en fonction d’une logique qui prend en compte les paramètres du système, de l’utilisateur et de l’application pour la langue de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4318-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="f4318-134">Ces attributs fondamentaux de l’interface MUI facilitent les scénarios d’entreprise tels que :</span><span class="sxs-lookup"><span data-stu-id="f4318-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="f4318-135">Un modèle de localisation amélioré pour l’interface utilisateur et le contenu de l’aide, grâce à la séparation physique du code source de l’application et des ressources localisables.</span><span class="sxs-lookup"><span data-stu-id="f4318-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="f4318-136">Traitement des ressources localisables en tant que contenu dynamique et chargement de celles-ci en fonction des paramètres de langue de l’interface utilisateur et des préférences de secours.</span><span class="sxs-lookup"><span data-stu-id="f4318-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="f4318-137">Cela permet des scénarios tels que :</span><span class="sxs-lookup"><span data-stu-id="f4318-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="f4318-138">Passage d’une langue d’interface utilisateur à une autre au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f4318-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="f4318-139">Création d’images de déploiement unique régionales ou mondiales qui couvrent un ensemble de langues pour les OEM et les entreprises.</span><span class="sxs-lookup"><span data-stu-id="f4318-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="f4318-140">Historique de MUI dans Windows</span><span class="sxs-lookup"><span data-stu-id="f4318-140">History of MUI in Windows</span></span>

<span data-ttu-id="f4318-141">Le niveau de prise en charge disponible pour une expérience utilisateur multilingue au niveau du système d’exploitation Windows et pour le développement d’applications multilingues sur la plate-forme Windows a évolué au fil du temps et dans les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="f4318-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="f4318-142">Les fonctionnalités prises en charge [avant Windows Vista](evolution-of-mui-support-across-windows-versions.md) étaient assez basiques, avec des images Windows en une seule langue et une option permettant d’ajouter des packs d’interface utilisateur multilingue dans des scénarios spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f4318-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="f4318-143">Aucune prise en charge de développeur pour les applications multilingues n’était disponible.</span><span class="sxs-lookup"><span data-stu-id="f4318-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="f4318-144">[Avec Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft a fait un investissement significatif dans MUI et Windows Vista est entièrement basé sur une plateforme MUI.</span><span class="sxs-lookup"><span data-stu-id="f4318-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="f4318-145">Bien que cela représente une avancée majeure dans la stratégie de localisation Windows, étant donné qu’il s’agit d’un activateur clé permettant à Microsoft de fournir des fenêtres dans un plus grand nombre de langues que jamais auparavant, il s’agit d’abord d’une grande avancée pour les utilisateurs, les développeurs et les clients Windows.</span><span class="sxs-lookup"><span data-stu-id="f4318-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="f4318-146">Il offre plusieurs avantages majeurs tels que :</span><span class="sxs-lookup"><span data-stu-id="f4318-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="f4318-147">Un système d’exploitation indépendant du langage avec prise en charge intégrée de MUI.</span><span class="sxs-lookup"><span data-stu-id="f4318-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="f4318-148">L’empaquetage, le déploiement et l’installation configurables pour prendre en charge les scénarios multilingues.</span><span class="sxs-lookup"><span data-stu-id="f4318-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="f4318-149">Déploiement d’une seule image avec plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="f4318-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="f4318-150">Modèle de maintenance amélioré dans lequel le code exécutable peut être mis à jour indépendamment des ressources.</span><span class="sxs-lookup"><span data-stu-id="f4318-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="f4318-151">Prise en charge des développeurs pour la création d’applications multilingues.</span><span class="sxs-lookup"><span data-stu-id="f4318-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="f4318-152">Le tableau suivant fournit une présentation détaillée de la prise en charge de la plateforme Windows pour MUI :</span><span class="sxs-lookup"><span data-stu-id="f4318-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4318-153">Category</span><span class="sxs-lookup"><span data-stu-id="f4318-153">Category</span></span></th>
<th><span data-ttu-id="f4318-154">Support</span><span class="sxs-lookup"><span data-stu-id="f4318-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f4318-155">Versions de Windows prises en charge (prise en charge du système d’exploitation uniquement)</span><span class="sxs-lookup"><span data-stu-id="f4318-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="f4318-156">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="f4318-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="f4318-157">Famille de serveurs Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f4318-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="f4318-158">Windows XP Professionnel</span><span class="sxs-lookup"><span data-stu-id="f4318-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="f4318-159">Windows XP Édition Tablet PC</span><span class="sxs-lookup"><span data-stu-id="f4318-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="f4318-160">Famille Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4318-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="f4318-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="f4318-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f4318-162">Versions de Windows prises en charge (système d’exploitation & application)</span><span class="sxs-lookup"><span data-stu-id="f4318-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="f4318-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4318-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f4318-164">Versions de Windows non prise en charge</span><span class="sxs-lookup"><span data-stu-id="f4318-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="f4318-165">Windows 9x</span><span class="sxs-lookup"><span data-stu-id="f4318-165">Windows 9x</span></span></li>
<li><span data-ttu-id="f4318-166">Windows me</span><span class="sxs-lookup"><span data-stu-id="f4318-166">Windows Me</span></span></li>
<li><span data-ttu-id="f4318-167">Windows XP Édition familiale</span><span class="sxs-lookup"><span data-stu-id="f4318-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="f4318-168">Avantages de la technologie MUI</span><span class="sxs-lookup"><span data-stu-id="f4318-168">Benefits of MUI technology</span></span>

<span data-ttu-id="f4318-169">MUI a un impact positif sur plusieurs aspects de l’écosystème Windows :</span><span class="sxs-lookup"><span data-stu-id="f4318-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="f4318-170">[Avantages pour les développeurs](benefits-of-mui-explained.md): de nombreux avantages sont offerts aux développeurs d’applications grâce à la disponibilité de la prise en charge de l’API MUI pour créer des applications multilingues modélisées selon les mêmes principes que la prise en charge multilingue dans le système d’exploitation Windows principal.</span><span class="sxs-lookup"><span data-stu-id="f4318-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="f4318-171">Les avantages sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f4318-171">These benefits include:</span></span>
    -   <span data-ttu-id="f4318-172">La possibilité de fournir une expérience de langue d’affichage conforme à ce que le système d’exploitation lui-même offre.</span><span class="sxs-lookup"><span data-stu-id="f4318-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="f4318-173">La possibilité d’étendre facilement la prise en charge linguistique pour une application.</span><span class="sxs-lookup"><span data-stu-id="f4318-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="f4318-174">La possibilité de gérer et de traiter facilement l’application.</span><span class="sxs-lookup"><span data-stu-id="f4318-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="f4318-175">La possibilité d’activer le déploiement d’une seule image d’applications par les fabricants d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="f4318-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="f4318-176">[Avantages pour les entreprises](benefits-of-mui-explained.md): le principal avantage que MUI offre aux entreprises est la possibilité de déployer, de prendre en charge et de conserver la même image multilingue dans le monde entier avec une seule installation.</span><span class="sxs-lookup"><span data-stu-id="f4318-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="f4318-177">Une autre victoire importante est la possibilité de prendre en charge des postes de travail multilingues qui offrent une interaction transparente aux utilisateurs avec différentes préférences linguistiques.</span><span class="sxs-lookup"><span data-stu-id="f4318-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="f4318-178">[Avantages pour les fabricants OEM](benefits-of-mui-explained.md): l’avantage majeur pour les OEM est l’installation d’image unique que MUI active, avec la prise en charge de plusieurs langues, ce qui permet une gestion plus efficace de l’inventaire.</span><span class="sxs-lookup"><span data-stu-id="f4318-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="f4318-179">Les OEM tirent également parti de la prise en charge MUI pour le développement d’applications, car elles permettent de fournir des applications à valeur ajoutée sur leurs images tout en bénéficiant de l’installation d’une seule image, à condition que ces applications soient compatibles avec l’interface MUI.</span><span class="sxs-lookup"><span data-stu-id="f4318-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 




