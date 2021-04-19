---
title: À propos de Windows Color System version 1.0
description: À propos de Windows Color System version 1.0
ms.assetid: 2a162840-660e-4a66-ad16-ef3c9b07925e
keywords:
- Windows Color System (WCS), à propos de
- WCS (système de couleurs Windows), à propos de
- gestion des couleurs des images, système de couleurs Windows (WCS)
- gestion des couleurs, système de couleurs Windows (WCS)
- couleurs, système de couleurs Windows (WCS)
- ICM (Image Color Management)
- ICM (gestion des couleurs d’image)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad2673f8b0943e16a1fbbacde11c4469d00b4e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106520213"
---
# <a name="about-windows-color-system-version-10"></a><span data-ttu-id="c3e47-110">À propos de Windows Color System version 1.0</span><span class="sxs-lookup"><span data-stu-id="c3e47-110">About Windows Color System Version 1.0</span></span>

<span data-ttu-id="c3e47-111">La technologie Microsoft Windows Color System (WCS) garantit qu’une image de couleur, un graphique ou un objet texte est rendu le plus près possible de son intention d’origine sur n’importe quel appareil, en dépit des différences entre les technologies d’imagerie et les capacités de couleur entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="c3e47-111">Microsoft Windows Color System (WCS) technology ensures that a color image, graphic or text object is rendered as close as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="c3e47-112">Que vous scanniez une image ou d’autres graphiques sur un scanneur de couleurs, que vous la téléchargeiez sur Internet, que vous la visualisiez ou la modifiiez à l’écran, que vous la déformiez sur du papier, sur un film ou sur un autre support, WCS 1,0 vous aide à conserver les couleurs cohérentes et précises.</span><span class="sxs-lookup"><span data-stu-id="c3e47-112">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it on the screen, or outputting it to paper, film, or other media, WCS 1.0 helps you keep its colors consistent and accurate.</span></span>

<span data-ttu-id="c3e47-113">WCS 1,0 fait partie intégrante de Microsoft Windows, car WCS 1,0 est intégré à la famille de systèmes d’exploitation Windows sous la forme d’un ensemble de fonctions d’API Win32, il est facilement disponible pour n’importe quelle application, pilote de périphérique, outil d’étalonnage de périphérique ou module de gestion des couleurs (CMM).</span><span class="sxs-lookup"><span data-stu-id="c3e47-113">WCS 1.0 is an integral part of Microsoft Windows Because WCS 1.0 is built into the Windows family of operating systems as a set of Win32 API functions, it is readily available to any application, device driver, device calibration tool, or color management module (CMM).</span></span>

<span data-ttu-id="c3e47-114">La version 1,0 de la gestion des couleurs des images (ICM) a été fournie dans Microsoft Windows 95 et fournit des fonctionnalités de gestion des couleurs de base dans les contextes de périphérique Windows.</span><span class="sxs-lookup"><span data-stu-id="c3e47-114">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="c3e47-115">ICM version 2,0 est inclus dans Windows 98, Windows Millennium Edition, Windows 2000 et Windows XP, ainsi que les fonctions incluses qui implémentent la gestion des couleurs en dehors des contextes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="c3e47-115">ICM version 2.0 is included in Windows 98, Windows Millennium Edition, Windows 2000, and Windows XP and included functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="c3e47-116">Ces fonctions étaient appropriées pour des exigences de gestion des couleurs plus exigeantes et offrent aux applications un meilleur contrôle sur le processus de gestion des couleurs.</span><span class="sxs-lookup"><span data-stu-id="c3e47-116">These functions were suitable for more demanding color management requirements, and give applications greater control over the color-management process.</span></span>

<span data-ttu-id="c3e47-117">WCS version 1,0 est inclus dans Windows Vista et comprend une variété de nouvelles fonctions qui fournissent des améliorations significatives en matière de flexibilité, de transparence, de prévisibilité et de extensibilité pour les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="c3e47-117">WCS version 1.0 is included in Windows Vista and includes a variety of new functions that provides significant improvements in flexiblity, transparency, predictability and extensiblity for vendors.</span></span>

<span data-ttu-id="c3e47-118">Quels sont les types d’applications qui tireront parti de l’utilisation du WCS 1,0 ?</span><span class="sxs-lookup"><span data-stu-id="c3e47-118">What kinds of applications will benefit from using WCS 1.0?</span></span> <span data-ttu-id="c3e47-119">Presque toutes les applications s’exécutant dans un environnement Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3e47-119">Almost any application running in a Windows Vista environment today.</span></span> <span data-ttu-id="c3e47-120">La fonctionnalité de gestion des couleurs de base est devenue une exigence pour les applications de toutes sortes.</span><span class="sxs-lookup"><span data-stu-id="c3e47-120">Basic color management capability is becoming a requirement for applications of all kinds.</span></span>

<span data-ttu-id="c3e47-121">L’affichage et l’impression des couleurs ont été améliorés au cours des dernières années jusqu’au moment où les images de couleur réalistes et les graphiques de couleurs complexes sont désormais couramment utilisés non seulement dans la publication sur le bureau, mais également dans un large éventail de données et d’applications de présentation.</span><span class="sxs-lookup"><span data-stu-id="c3e47-121">Color display and printing have improved in recent years to the point where photo-realistic color images and complex color graphics are now commonly used not only in desktop publishing, but also across a broad spectrum of data and presentation applications.</span></span> <span data-ttu-id="c3e47-122">Les technologies d’objets telles que COM et ActiveX ont des objets de couleur incorporés dans pratiquement tous les types d’espace de données.</span><span class="sxs-lookup"><span data-stu-id="c3e47-122">Object technologies such as COM and ActiveX have embedded color objects in virtually every kind of data space.</span></span>

<span data-ttu-id="c3e47-123">Les catalogues d’habillement, l’art en ligne, les albums photo de famille, les logos d’entreprise, les graphiques, les graphiques, les présentations, les aperçus d’impression et les simulations de couleurs sont quelques exemples d’applications quotidiennes pour lesquelles la couleur est importante.</span><span class="sxs-lookup"><span data-stu-id="c3e47-123">Clothing catalogs, online art, family photo albums, business logos, charts, graphs, presentations, print previews, and color simulations are just a few examples of everyday applications where color matters.</span></span>

<span data-ttu-id="c3e47-124">Par conséquent, de plus en plus d’utilisateurs requièrent que leurs applications soient en mesure d’afficher fidèlement les couleurs.</span><span class="sxs-lookup"><span data-stu-id="c3e47-124">As a result, more and more users are requiring their applications to be capable of accurate color display.</span></span> <span data-ttu-id="c3e47-125">Un rendu des couleurs médiocre Ruins les images et les graphiques qui sont de plus en plus importants pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c3e47-125">Poor color rendering ruins the images and graphics that are increasingly important to users.</span></span>

<span data-ttu-id="c3e47-126">À un niveau fondamental, presque toutes les applications doivent être en mesure d’ajuster automatiquement la couleur afin que sa sortie soit identique sur les différents moniteurs et imprimantes.</span><span class="sxs-lookup"><span data-stu-id="c3e47-126">On a fundamental level, almost any application should be able to adjust color automatically so that its output looks the same on different monitors and printers.</span></span> <span data-ttu-id="c3e47-127">WCS 1,0 fournit un ensemble de fonctions pour fournir ce type de gestion des couleurs qui est transparent pour un utilisateur et nécessite une faible surcharge dans l’application.</span><span class="sxs-lookup"><span data-stu-id="c3e47-127">WCS 1.0 provides a set of functions to deliver this kind of color management that is transparent to a user and requires little overhead in the application.</span></span>

<span data-ttu-id="c3e47-128">À un niveau supérieur, WCS 1,0 fournit des fonctions supplémentaires qui fournissent une gestion des couleurs plus complexe et contrôlable.</span><span class="sxs-lookup"><span data-stu-id="c3e47-128">On a higher level, WCS 1.0 provides additional functions that deliver more complex and controllable color management.</span></span> <span data-ttu-id="c3e47-129">Les applications graphiques et de publication de bureau ont besoin de ces fonctionnalités supplémentaires pour permettre à leurs utilisateurs de travailler avec précision sur de nombreux appareils tout au long d’un processus de production.</span><span class="sxs-lookup"><span data-stu-id="c3e47-129">Graphics and desktop publishing applications need these additional capabilities to let their users work precisely with consistent color across many devices throughout a production process.</span></span>

<span data-ttu-id="c3e47-130">En règle générale, les fournisseurs de logiciels dont les produits sont en couleur ou en sortie et les fournisseurs de matériel des périphériques de couleur trouveront le WCS 1,0 une technologie clé pour simplifier la livraison de produits réussis.</span><span class="sxs-lookup"><span data-stu-id="c3e47-130">In general, software vendors whose products deal with color input or output and hardware vendors of color peripherals will find WCS 1.0 a key technology for simplifying the delivery of successful products.</span></span> <span data-ttu-id="c3e47-131">Les sections suivantes incluent :</span><span class="sxs-lookup"><span data-stu-id="c3e47-131">The following sections include:</span></span>

-   [<span data-ttu-id="c3e47-132">Nouveautés de la version 1.0 de WCS</span><span class="sxs-lookup"><span data-stu-id="c3e47-132">What's New in Version 1.0 of WCS</span></span>](what-s-new-in-version-1-0-of-wcs.md)
-   [<span data-ttu-id="c3e47-133">Disponibilité de WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="c3e47-133">WCS 1.0 Availability</span></span>](wcs-1-0-availability.md)

 

 




