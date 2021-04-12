---
description: Composant Windows Imaging
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Composant Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203804"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="90cbd-103">Composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="90cbd-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="90cbd-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="90cbd-104">Purpose</span></span>

<span data-ttu-id="90cbd-105">Le composant WIC (Windows Imaging Component) est une plateforme extensible qui fournit une API de bas niveau pour les images numériques.</span><span class="sxs-lookup"><span data-stu-id="90cbd-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="90cbd-106">WIC prend en charge les formats d’image Web standard, les images de plage dynamique élevée et les données d’appareil photo brutes.</span><span class="sxs-lookup"><span data-stu-id="90cbd-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="90cbd-107">WIC prend également en charge des fonctionnalités supplémentaires telles que :</span><span class="sxs-lookup"><span data-stu-id="90cbd-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="90cbd-108">Prise en charge intégrée des formats de métadonnées standard</span><span class="sxs-lookup"><span data-stu-id="90cbd-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="90cbd-109">Framework extensible pour les codecs d’image, les formats de pixel et les formats de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="90cbd-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="90cbd-110">Large éventail de prise en charge du format de pixel.</span><span class="sxs-lookup"><span data-stu-id="90cbd-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="90cbd-111">Prise en charge des couleurs élevées ; y compris les formats de pixels étendus 30 bits, haute précision 30 bits et haute précision 48 bits et à large gamme.</span><span class="sxs-lookup"><span data-stu-id="90cbd-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="90cbd-112">Décodage d’image progressif.</span><span class="sxs-lookup"><span data-stu-id="90cbd-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="90cbd-113">Public de développeurs</span><span class="sxs-lookup"><span data-stu-id="90cbd-113">Developer Audience</span></span>

<span data-ttu-id="90cbd-114">WIC est conçu pour répondre aux besoins des classes de développeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90cbd-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="90cbd-115">Développeurs qui lisent et écrivent des données d’image dans une application.</span><span class="sxs-lookup"><span data-stu-id="90cbd-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="90cbd-116">Développeurs qui lisent et écrivent des métadonnées d’image dans une application.</span><span class="sxs-lookup"><span data-stu-id="90cbd-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="90cbd-117">Les développeurs qui souhaitent la détection de codecs à l’exécution pour les codecs d’image récemment conçus ou implémentés.</span><span class="sxs-lookup"><span data-stu-id="90cbd-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="90cbd-118">Les développeurs qui conçoivent ou implémentent de nouveaux codecs d’image et des formats de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="90cbd-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="90cbd-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="90cbd-119">In this section</span></span>



| <span data-ttu-id="90cbd-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="90cbd-120">Topic</span></span>                                                                 | <span data-ttu-id="90cbd-121">Description</span><span class="sxs-lookup"><span data-stu-id="90cbd-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="90cbd-122">Nouveautés de WIC</span><span class="sxs-lookup"><span data-stu-id="90cbd-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="90cbd-123">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="90cbd-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="90cbd-124">Décrit comment utiliser les API WIC.</span><span class="sxs-lookup"><span data-stu-id="90cbd-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="90cbd-125">Référence</span><span class="sxs-lookup"><span data-stu-id="90cbd-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="90cbd-126">Contient la référence pour les API WIC.</span><span class="sxs-lookup"><span data-stu-id="90cbd-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="90cbd-127">Exemples WIC</span><span class="sxs-lookup"><span data-stu-id="90cbd-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="90cbd-128">Fournit des exemples pour WIC.</span><span class="sxs-lookup"><span data-stu-id="90cbd-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="90cbd-129">Glossaire</span><span class="sxs-lookup"><span data-stu-id="90cbd-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="90cbd-130">Définit les termes utilisés dans WIC.</span><span class="sxs-lookup"><span data-stu-id="90cbd-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




