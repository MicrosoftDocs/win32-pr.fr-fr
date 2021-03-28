---
description: Une application remplit l’intérieur d’une région en appelant la fonction FillRgn et en fournissant un handle qui identifie un pinceau spécifique.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Remplissage des régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034220"
---
# <a name="filling-regions"></a><span data-ttu-id="a19ab-103">Remplissage des régions</span><span class="sxs-lookup"><span data-stu-id="a19ab-103">Filling Regions</span></span>

<span data-ttu-id="a19ab-104">Une application remplit l’intérieur d’une région en appelant la fonction [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) et en fournissant un handle qui identifie un pinceau spécifique.</span><span class="sxs-lookup"><span data-stu-id="a19ab-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="a19ab-105">Quand une application appelle FillRgn, le système remplit la région avec le pinceau en utilisant le mode de remplissage actuel pour le contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="a19ab-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="a19ab-106">Il existe deux modes de remplissage : alternative et enroulement.</span><span class="sxs-lookup"><span data-stu-id="a19ab-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="a19ab-107">L’application peut définir le mode de remplissage pour un contexte de périphérique en appelant la fonction [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="a19ab-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="a19ab-108">L’application peut récupérer le mode de remplissage actuel pour un contexte de périphérique en appelant la fonction [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="a19ab-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="a19ab-109">L’illustration suivante montre deux régions identiques : l’une remplie à l’aide du mode alternatif et l’autre remplie à l’aide du mode enroulement.</span><span class="sxs-lookup"><span data-stu-id="a19ab-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![Illustration montrant des étoiles de 2 5 : une remplie uniquement en points, l’autre remplie entièrement](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="a19ab-111">Mode alternatif</span><span class="sxs-lookup"><span data-stu-id="a19ab-111">Alternate Mode</span></span>

<span data-ttu-id="a19ab-112">Pour déterminer les pixels que le système met en surbrillance lorsque le mode alternatif est spécifié, effectuez le test suivant :</span><span class="sxs-lookup"><span data-stu-id="a19ab-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="a19ab-113">Sélectionnez un pixel dans l’intérieur de la région.</span><span class="sxs-lookup"><span data-stu-id="a19ab-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="a19ab-114">Dessinez un rayon imaginaire, dans l’axe x positif, de ce pixel vers l’infini.</span><span class="sxs-lookup"><span data-stu-id="a19ab-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="a19ab-115">Chaque fois que le rayon croise une ligne de limite, Incrémentez une valeur de nombre.</span><span class="sxs-lookup"><span data-stu-id="a19ab-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="a19ab-116">Le système met en surbrillance le pixel si la valeur de nombre est un nombre impair.</span><span class="sxs-lookup"><span data-stu-id="a19ab-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="a19ab-117">Mode de bobinage</span><span class="sxs-lookup"><span data-stu-id="a19ab-117">Winding Mode</span></span>

<span data-ttu-id="a19ab-118">Pour déterminer les pixels que le système met en surbrillance lorsque le mode d’enroulement est spécifié, effectuez le test suivant :</span><span class="sxs-lookup"><span data-stu-id="a19ab-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="a19ab-119">Déterminez la direction dans laquelle chaque ligne de limite est dessinée.</span><span class="sxs-lookup"><span data-stu-id="a19ab-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="a19ab-120">Sélectionnez un pixel dans l’intérieur de la région.</span><span class="sxs-lookup"><span data-stu-id="a19ab-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="a19ab-121">Dessinez un rayon imaginaire, dans l’axe x positif, du pixel vers l’infini.</span><span class="sxs-lookup"><span data-stu-id="a19ab-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="a19ab-122">Chaque fois que le rayon croise une ligne de limite avec un composant y positif, Incrémentez une valeur de nombre.</span><span class="sxs-lookup"><span data-stu-id="a19ab-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="a19ab-123">Chaque fois que le rayon croise une ligne de limite avec un composant y négatif, décrémente la valeur du nombre.</span><span class="sxs-lookup"><span data-stu-id="a19ab-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="a19ab-124">Le système met en surbrillance le pixel si la valeur de nombre est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a19ab-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



