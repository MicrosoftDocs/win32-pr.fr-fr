---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8223ec5e98db3e45b0087073b4eb68baeae81280
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089177"
---
# <a name="direct2d"></a><span data-ttu-id="9222e-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="9222e-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="9222e-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="9222e-104">Purpose</span></span>

<span data-ttu-id="9222e-105">Direct2D est une API graphique 2D à accélération matérielle et en mode immédiat, qui offre des performances élevées et un rendu de grande qualité pour les éléments géométriques, bitmaps et textes 2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="9222e-106">L’API Direct2D est conçue pour interagir correctement avec GDI, GDI+ et Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9222e-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9222e-107">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="9222e-107">Developer audience</span></span>

<span data-ttu-id="9222e-108">Direct2D est principalement conçu pour être utilisé par les classes de développeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9222e-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="9222e-109">Développeurs de grandes applications natives à l’échelle de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9222e-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="9222e-110">Les développeurs qui créent des outils de contrôle et des bibliothèques pour la consommation par les développeurs en aval.</span><span class="sxs-lookup"><span data-stu-id="9222e-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="9222e-111">Développeurs qui ont besoin d’un rendu côté serveur d’un graphique 2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="9222e-112">Les développeurs qui utilisent les graphiques Direct3D et ont besoin d’un rendu de texte et de langage 2D simple et hautes performances pour les menus, les éléments d’interface utilisateur et les affichages des têtes (HUDs).</span><span class="sxs-lookup"><span data-stu-id="9222e-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9222e-113">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="9222e-113">Run-time requirements</span></span>

-   <span data-ttu-id="9222e-114">Windows 7 ou Windows Vista avec Service Pack 2 (SP2) et mise à jour de la plateforme pour Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9222e-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="9222e-115">Windows Server 2008 R2 ou Windows Server 2008 avec Service Pack 2 (SP2) et la mise à jour de la plateforme pour Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9222e-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="9222e-116">La mise à jour de plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 sont un ensemble de bibliothèques d’exécution qui permet aux développeurs de cibler des applications sur Windows 7, Windows Vista, Windows Server 2008 R2 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9222e-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="9222e-117">Ces mises à jour seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="9222e-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="9222e-118">Les applications tierces qui requièrent une mise à jour de plateforme pour Windows Vista ou une mise à jour de plateforme pour Windows Server 2008 peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9222e-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="9222e-119">Pour plus d’informations sur les deux mises à jour, consultez [mise à jour de la plateforme pour Windows Vista](https://support.microsoft.com/kb/971644).</span><span class="sxs-lookup"><span data-stu-id="9222e-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="9222e-120">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9222e-120">In this section</span></span>



| <span data-ttu-id="9222e-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9222e-121">Topic</span></span>                                                                                          | <span data-ttu-id="9222e-122">Description</span><span class="sxs-lookup"><span data-stu-id="9222e-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9222e-123">Nouveautés de Direct2D</span><span class="sxs-lookup"><span data-stu-id="9222e-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="9222e-124">Voici quelques-uns des nouveaux ajouts à Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="9222e-125">À propos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="9222e-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="9222e-126">Introduit Direct2D, une API qui fournit aux développeurs Win32 la possibilité d’effectuer des tâches de rendu graphiques 2D avec des performances et une qualité visuel supérieures.</span><span class="sxs-lookup"><span data-stu-id="9222e-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="9222e-127">Démarrage rapide de Direct2D pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="9222e-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="9222e-128">Résume les étapes requises pour dessiner avec Direct2D et fournit un exemple de code.</span><span class="sxs-lookup"><span data-stu-id="9222e-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9222e-129">Prise en main avec Direct2D</span><span class="sxs-lookup"><span data-stu-id="9222e-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="9222e-130">Décrit comment prendre en main la création d’applications Direct2D et fournit un exemple de code.</span><span class="sxs-lookup"><span data-stu-id="9222e-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="9222e-131">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="9222e-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="9222e-132">Cette section contient des rubriques de programmation conceptuelle qui décrivent comment utiliser l’API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="9222e-133">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="9222e-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="9222e-134">Décrit en détail l’API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="9222e-135">Outils et utilitaires</span><span class="sxs-lookup"><span data-stu-id="9222e-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="9222e-136">Outils et utilitaires fournis pour Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="9222e-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="9222e-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="9222e-138">Exemples d’applications qui illustrent l’API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="9222e-139">Glossaire Direct2D</span><span class="sxs-lookup"><span data-stu-id="9222e-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="9222e-140">Décrit les termes couramment utilisés par la documentation Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9222e-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="9222e-141">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9222e-141">Additional resources</span></span>

-   [<span data-ttu-id="9222e-142">**Graphiques et jeux DirectX**</span><span class="sxs-lookup"><span data-stu-id="9222e-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="9222e-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="9222e-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

