---
title: Indicateurs de création de transformation CMM
description: CMMs utilise les indicateurs de création de transformation comme indicateurs pour la création d’une transformation de couleur. Il revient à la méthode CMM de déterminer la meilleure façon d’utiliser ces indicateurs.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "106522482"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="4c387-104">Indicateurs de création de transformation CMM</span><span class="sxs-lookup"><span data-stu-id="4c387-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="4c387-105">CMMs utilise les indicateurs de création de transformation comme indicateurs pour la création d’une transformation de couleur.</span><span class="sxs-lookup"><span data-stu-id="4c387-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="4c387-106">Il revient à la méthode CMM de déterminer la meilleure façon d’utiliser ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4c387-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="4c387-107">Toutes les fonctions qui utilisent ces indicateurs passent ou reçoivent des valeurs d’indicateur via un paramètre appelé *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="4c387-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="4c387-108">Le **mot** de poids fort de *dwFlags* doit être défini sur une valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4c387-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="4c387-109">Constante</span><span class="sxs-lookup"><span data-stu-id="4c387-109">Constant</span></span>                    | <span data-ttu-id="4c387-110">Description</span><span class="sxs-lookup"><span data-stu-id="4c387-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c387-111">ACTIVER la vérification de la \_ gamme \_</span><span class="sxs-lookup"><span data-stu-id="4c387-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="4c387-112">Utilisez cette transformation pour la vérification de la gamme de couleurs.</span><span class="sxs-lookup"><span data-stu-id="4c387-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="4c387-113">UTILISER \_ \_ Colorimétrie relative</span><span class="sxs-lookup"><span data-stu-id="4c387-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="4c387-114">Ne conservez pas le point blanc.</span><span class="sxs-lookup"><span data-stu-id="4c387-114">Do not preserve the white point.</span></span> <span data-ttu-id="4c387-115">Si la gamme de sortie ne prend pas en charge une couleur donnée, utilisez la couleur la plus proche prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4c387-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="4c387-116">Consultez rendu des intentions.</span><span class="sxs-lookup"><span data-stu-id="4c387-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="4c387-117">\_traduction rapide</span><span class="sxs-lookup"><span data-stu-id="4c387-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="4c387-118">Rechercher uniquement la couleur.</span><span class="sxs-lookup"><span data-stu-id="4c387-118">Look up color only.</span></span> <span data-ttu-id="4c387-119">N’interpolez pas la couleur.</span><span class="sxs-lookup"><span data-stu-id="4c387-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="4c387-120">PRESERVEBLACK</span><span class="sxs-lookup"><span data-stu-id="4c387-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="4c387-121">Insère le GMMP de génération noir approprié comme dernier GMMP dans la séquence de transformation</span><span class="sxs-lookup"><span data-stu-id="4c387-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="4c387-122">\_toujours WCS</span><span class="sxs-lookup"><span data-stu-id="4c387-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="4c387-123">Utilisez le chemin de code WCS même pour les transformations ICC.</span><span class="sxs-lookup"><span data-stu-id="4c387-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="4c387-124">\_transformation séquentielle</span><span class="sxs-lookup"><span data-stu-id="4c387-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="4c387-125">Indicateur de création de transformation pour la création d’une transformation de couleur séquentielle (non optimisée).</span><span class="sxs-lookup"><span data-stu-id="4c387-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="4c387-126">Le **mot** de poids faible peut avoir l’une des valeurs constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4c387-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="4c387-127">Constante</span><span class="sxs-lookup"><span data-stu-id="4c387-127">Constant</span></span>     | <span data-ttu-id="4c387-128">Description</span><span class="sxs-lookup"><span data-stu-id="4c387-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c387-129">MODE de vérification \_</span><span class="sxs-lookup"><span data-stu-id="4c387-129">PROOF\_MODE</span></span>  | <span data-ttu-id="4c387-130">La transformation sera utilisée pour afficher un aperçu de l’image.</span><span class="sxs-lookup"><span data-stu-id="4c387-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="4c387-131">Qualité d’image faible.</span><span class="sxs-lookup"><span data-stu-id="4c387-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="4c387-132">\_mode normal</span><span class="sxs-lookup"><span data-stu-id="4c387-132">NORMAL\_MODE</span></span> | <span data-ttu-id="4c387-133">La transformation sera utilisée pour l’affichage normal de l’image.</span><span class="sxs-lookup"><span data-stu-id="4c387-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="4c387-134">Qualité d’image moyenne.</span><span class="sxs-lookup"><span data-stu-id="4c387-134">Average image quality.</span></span>                            |
| <span data-ttu-id="4c387-135">MEILLEUR \_ mode</span><span class="sxs-lookup"><span data-stu-id="4c387-135">BEST\_MODE</span></span>   | <span data-ttu-id="4c387-136">La transformation sera utilisée pour l’affichage de l’image de qualité supérieure possible sur l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="4c387-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="4c387-137">En passant du \_ mode preuve au meilleur \_ mode, la qualité de la sortie s’améliore généralement et la vitesse de transformation diminue.</span><span class="sxs-lookup"><span data-stu-id="4c387-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c387-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c387-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c387-139">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="4c387-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="4c387-140">Constantes ICM</span><span class="sxs-lookup"><span data-stu-id="4c387-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




