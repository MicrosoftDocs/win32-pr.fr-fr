---
title: Référence du mode de format BC7
description: Cette documentation contient la liste des 8 modes de blocage et des allocations de bits pour les blocs de format de compression de texture BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "104381362"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="79ea2-103">Référence du mode de format BC7</span><span class="sxs-lookup"><span data-stu-id="79ea2-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="79ea2-104">Cette documentation contient la liste des 8 modes de blocage et des allocations de bits pour les blocs de format de compression de texture BC7.</span><span class="sxs-lookup"><span data-stu-id="79ea2-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="79ea2-105">Les couleurs de chaque sous-ensemble au sein d’un bloc sont représentées par deux couleurs de point de terminaison explicites et un ensemble de couleurs interpolées entre elles.</span><span class="sxs-lookup"><span data-stu-id="79ea2-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="79ea2-106">Selon la précision de l’index du bloc, chaque sous-ensemble peut avoir 4, 8 ou 16 couleurs possibles.</span><span class="sxs-lookup"><span data-stu-id="79ea2-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="79ea2-107">Mode 0</span><span class="sxs-lookup"><span data-stu-id="79ea2-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="79ea2-108">Mode 1</span><span class="sxs-lookup"><span data-stu-id="79ea2-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="79ea2-109">Mode 2</span><span class="sxs-lookup"><span data-stu-id="79ea2-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="79ea2-110">Mode 3</span><span class="sxs-lookup"><span data-stu-id="79ea2-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="79ea2-111">Mode 4</span><span class="sxs-lookup"><span data-stu-id="79ea2-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="79ea2-112">Mode 5</span><span class="sxs-lookup"><span data-stu-id="79ea2-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="79ea2-113">Mode 6</span><span class="sxs-lookup"><span data-stu-id="79ea2-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="79ea2-114">Mode 7</span><span class="sxs-lookup"><span data-stu-id="79ea2-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="79ea2-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="79ea2-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="79ea2-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79ea2-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="79ea2-117">Mode 0</span><span class="sxs-lookup"><span data-stu-id="79ea2-117">Mode 0</span></span>

<span data-ttu-id="79ea2-118">Le mode BC7 0 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-119">Composants de couleur uniquement (sans alpha)</span><span class="sxs-lookup"><span data-stu-id="79ea2-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="79ea2-120">3 sous-ensembles par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-120">3 subsets per block</span></span>
-   <span data-ttu-id="79ea2-121">Points de terminaison RGBP 4.4.4.1 avec un bit P unique par point de terminaison</span><span class="sxs-lookup"><span data-stu-id="79ea2-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="79ea2-122">index 3 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-122">3-bit indices</span></span>
-   <span data-ttu-id="79ea2-123">16 partitions</span><span class="sxs-lookup"><span data-stu-id="79ea2-123">16 partitions</span></span>

![disposition en mode 0 bits](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="79ea2-125">Mode 1</span><span class="sxs-lookup"><span data-stu-id="79ea2-125">Mode 1</span></span>

<span data-ttu-id="79ea2-126">BC7 mode 1 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-127">Composants de couleur uniquement (sans alpha)</span><span class="sxs-lookup"><span data-stu-id="79ea2-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="79ea2-128">2 sous-ensembles par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-128">2 subsets per block</span></span>
-   <span data-ttu-id="79ea2-129">Points de terminaison RGBP 6.6.6.1 avec un bit P partagé par sous-ensemble)</span><span class="sxs-lookup"><span data-stu-id="79ea2-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="79ea2-130">index 3 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-130">3-bit indices</span></span>
-   <span data-ttu-id="79ea2-131">64 partitions</span><span class="sxs-lookup"><span data-stu-id="79ea2-131">64 partitions</span></span>

![disposition 1 bit mode](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="79ea2-133">Mode 2</span><span class="sxs-lookup"><span data-stu-id="79ea2-133">Mode 2</span></span>

<span data-ttu-id="79ea2-134">Le mode BC7 2 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-135">Composants de couleur uniquement (sans alpha)</span><span class="sxs-lookup"><span data-stu-id="79ea2-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="79ea2-136">3 sous-ensembles par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-136">3 subsets per block</span></span>
-   <span data-ttu-id="79ea2-137">Points de terminaison 5.5.5 RVB</span><span class="sxs-lookup"><span data-stu-id="79ea2-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="79ea2-138">index 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-138">2-bit indices</span></span>
-   <span data-ttu-id="79ea2-139">64 partitions</span><span class="sxs-lookup"><span data-stu-id="79ea2-139">64 partitions</span></span>

![disposition en mode 2 bits](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="79ea2-141">Mode 3</span><span class="sxs-lookup"><span data-stu-id="79ea2-141">Mode 3</span></span>

<span data-ttu-id="79ea2-142">Le mode BC7 3 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-143">Composants de couleur uniquement (sans alpha)</span><span class="sxs-lookup"><span data-stu-id="79ea2-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="79ea2-144">2 sous-ensembles par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-144">2 subsets per block</span></span>
-   <span data-ttu-id="79ea2-145">Points de terminaison RGBP 7.7.7.1 avec un bit P unique par sous-ensemble)</span><span class="sxs-lookup"><span data-stu-id="79ea2-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="79ea2-146">index 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-146">2-bit indices</span></span>
-   <span data-ttu-id="79ea2-147">64 partitions</span><span class="sxs-lookup"><span data-stu-id="79ea2-147">64 partitions</span></span>

![disposition en mode 3 bits](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="79ea2-149">Mode 4</span><span class="sxs-lookup"><span data-stu-id="79ea2-149">Mode 4</span></span>

<span data-ttu-id="79ea2-150">Le mode BC7 4 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-151">Composants de couleur avec composant alpha distinct</span><span class="sxs-lookup"><span data-stu-id="79ea2-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="79ea2-152">1 sous-ensemble par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-152">1 subset per block</span></span>
-   <span data-ttu-id="79ea2-153">Points de terminaison de couleur RVB 5.5.5</span><span class="sxs-lookup"><span data-stu-id="79ea2-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="79ea2-154">points de terminaison alpha 6 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="79ea2-155">16 x index 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="79ea2-156">16 x index 3 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="79ea2-157">rotation des composants 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-157">2-bit component rotation</span></span>
-   <span data-ttu-id="79ea2-158">sélecteur d’index 1 bit (si les index à 2 ou 3 bits sont utilisés)</span><span class="sxs-lookup"><span data-stu-id="79ea2-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![disposition en mode 4 bits](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="79ea2-160">Mode 5</span><span class="sxs-lookup"><span data-stu-id="79ea2-160">Mode 5</span></span>

<span data-ttu-id="79ea2-161">Le mode BC7 5 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-162">Composants de couleur avec composant alpha distinct</span><span class="sxs-lookup"><span data-stu-id="79ea2-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="79ea2-163">1 sous-ensemble par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-163">1 subset per block</span></span>
-   <span data-ttu-id="79ea2-164">Points de terminaison de couleur RVB 7.7.7</span><span class="sxs-lookup"><span data-stu-id="79ea2-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="79ea2-165">points de terminaison alpha 8 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="79ea2-166">16 x index de couleurs 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="79ea2-167">16 x index alpha 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="79ea2-168">rotation des composants 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-168">2-bit component rotation</span></span>

![disposition en mode 5 bits](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="79ea2-170">Mode 6</span><span class="sxs-lookup"><span data-stu-id="79ea2-170">Mode 6</span></span>

<span data-ttu-id="79ea2-171">Le mode BC7 6 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-172">Composants de couleur et alpha combinés</span><span class="sxs-lookup"><span data-stu-id="79ea2-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="79ea2-173">Un seul sous-ensemble par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-173">One subset per block</span></span>
-   <span data-ttu-id="79ea2-174">Points de terminaison de couleur RGBAP 7.7.7.7.1 (et alpha) (P-bit unique par point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="79ea2-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="79ea2-175">16 x index 4 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-175">16 x 4-bit indices</span></span>

![disposition en mode 6 bits](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="79ea2-177">Mode 7</span><span class="sxs-lookup"><span data-stu-id="79ea2-177">Mode 7</span></span>

<span data-ttu-id="79ea2-178">Le mode BC7 7 présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="79ea2-179">Composants de couleur et alpha combinés</span><span class="sxs-lookup"><span data-stu-id="79ea2-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="79ea2-180">2 sous-ensembles par bloc</span><span class="sxs-lookup"><span data-stu-id="79ea2-180">2 subsets per block</span></span>
-   <span data-ttu-id="79ea2-181">Points de terminaison de couleur RGBAP 5.5.5.5.1 (et alpha) (P-bit unique par point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="79ea2-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="79ea2-182">index 2 bits</span><span class="sxs-lookup"><span data-stu-id="79ea2-182">2-bit indices</span></span>
-   <span data-ttu-id="79ea2-183">64 partitions</span><span class="sxs-lookup"><span data-stu-id="79ea2-183">64 partitions</span></span>

![disposition en mode 7 bits](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="79ea2-185">Notes</span><span class="sxs-lookup"><span data-stu-id="79ea2-185">Remarks</span></span>

<span data-ttu-id="79ea2-186">Le mode 8 (l’octet le moins significatif est défini sur 0x00) est réservé.</span><span class="sxs-lookup"><span data-stu-id="79ea2-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="79ea2-187">Ne l’utilisez pas dans votre encodeur.</span><span class="sxs-lookup"><span data-stu-id="79ea2-187">Don't use it in your encoder.</span></span> <span data-ttu-id="79ea2-188">Si vous transmettez ce mode au matériel, un bloc initialisé à tous les zéros est retourné.</span><span class="sxs-lookup"><span data-stu-id="79ea2-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="79ea2-189">Dans BC7, vous pouvez encoder le composant alpha de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="79ea2-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="79ea2-190">Types de bloc sans encodage de composant alpha explicite.</span><span class="sxs-lookup"><span data-stu-id="79ea2-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="79ea2-191">Dans ces blocs, les points de terminaison de couleur ont un encodage RVB uniquement, le composant alpha étant décodé sur 1,0 pour tous les éléments de texture.</span><span class="sxs-lookup"><span data-stu-id="79ea2-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="79ea2-192">Types de blocs avec des composants alpha et de couleur combinés.</span><span class="sxs-lookup"><span data-stu-id="79ea2-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="79ea2-193">Dans ces blocs, les valeurs de couleur du point de terminaison sont spécifiées au format RVBA et les valeurs des composants alpha sont interpolées avec les valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="79ea2-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="79ea2-194">Types de bloc avec des composants alpha et de couleur séparés.</span><span class="sxs-lookup"><span data-stu-id="79ea2-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="79ea2-195">Dans ces blocs, les valeurs de couleur et alpha sont spécifiées séparément, chacune avec son propre jeu d’index.</span><span class="sxs-lookup"><span data-stu-id="79ea2-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="79ea2-196">Par conséquent, ils ont un vecteur effectif et un canal scalaire qui sont encodés séparément, où le vecteur spécifie généralement les canaux \[ de couleur R, G, B \] et le scalaire spécifie le canal alpha \[ a \] .</span><span class="sxs-lookup"><span data-stu-id="79ea2-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="79ea2-197">Pour prendre en charge cette approche, un champ 2 bits distinct est fourni dans l’encodage, qui permet la spécification de l’encodage de canal distinct comme valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="79ea2-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="79ea2-198">Par conséquent, le bloc peut avoir l’une des quatre représentations suivantes de cet encodage alpha (comme indiqué par le champ de 2 bits) :</span><span class="sxs-lookup"><span data-stu-id="79ea2-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="79ea2-199">RVB \| A : canal alpha distinct</span><span class="sxs-lookup"><span data-stu-id="79ea2-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="79ea2-200">AGB \| R : canal de couleur « rouge » distinct</span><span class="sxs-lookup"><span data-stu-id="79ea2-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="79ea2-201">RAB \| G : canal de couleur « vert » distinct</span><span class="sxs-lookup"><span data-stu-id="79ea2-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="79ea2-202">RGA \| B : canal de couleur « bleu » distinct</span><span class="sxs-lookup"><span data-stu-id="79ea2-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="79ea2-203">Le décodeur réorganise l’ordre des canaux à la valeur RVBA après le décodage, de sorte que le format de bloc interne est invisible pour le développeur.</span><span class="sxs-lookup"><span data-stu-id="79ea2-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="79ea2-204">Les noirs avec des composants alpha et de couleur distincts ont également deux jeux de données d’index : un pour l’ensemble vectorisé de canaux et un pour le canal scalaire.</span><span class="sxs-lookup"><span data-stu-id="79ea2-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="79ea2-205">(Dans le cas du mode 4, ces index sont de largeur différente de \[ 2 ou 3 bits \] .</span><span class="sxs-lookup"><span data-stu-id="79ea2-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="79ea2-206">Le mode 4 contient également un sélecteur 1 bit qui spécifie si le vecteur ou le canal scalaire utilise les index 3 bits.</span><span class="sxs-lookup"><span data-stu-id="79ea2-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="79ea2-207">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79ea2-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79ea2-208">Format BC7</span><span class="sxs-lookup"><span data-stu-id="79ea2-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




