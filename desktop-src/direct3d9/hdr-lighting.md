---
description: L’éclairage dans le monde réel contient une plage dynamique très élevée (HDR) de valeurs de luminance.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Éclairage HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200639"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="7fb60-103">Éclairage HDR (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7fb60-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="7fb60-104">L’éclairage dans le monde réel contient une plage dynamique très élevée (HDR) de valeurs de luminance.</span><span class="sxs-lookup"><span data-stu-id="7fb60-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="7fb60-105">Le monde réel compte environ 10 commandes de plages dynamiques (DR) pour les valeurs de luminance réparties dans le spectre d’obscurité à la luminosité.</span><span class="sxs-lookup"><span data-stu-id="7fb60-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="7fb60-106">En revanche, un écran d’ordinateur a une gamme d’affichage très limitée (ou une plage de valeurs de luminance) : environ deux commandes de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="7fb60-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="7fb60-107">La difficulté à produire des images de rendu HDR consiste à mapper les valeurs HDR réelles dans la gamme limitée d’un écran d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7fb60-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="7fb60-108">Le mappage de tonalité est la technique utilisée par DirectX pour mapper les informations HDR dans une plage plus limitée.</span><span class="sxs-lookup"><span data-stu-id="7fb60-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="7fb60-109">Le mappage de tonalité appliqué au rendu CGI peut améliorer considérablement la quantité de détails d’éclairage rendue, ce qui permet d’afficher des détails dans les zones les plus sombres et de fournir un contraste dans les zones qui sont tellement brillantes.</span><span class="sxs-lookup"><span data-stu-id="7fb60-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="7fb60-110">Les scènes résultantes sont rendues avec des détails d’éclairage bien plus visibles.</span><span class="sxs-lookup"><span data-stu-id="7fb60-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="7fb60-111">L' [exemple HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) est un kit de développement logiciel (SDK) qui illustre l’éclairage HDR.</span><span class="sxs-lookup"><span data-stu-id="7fb60-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="7fb60-112">Correspondance des tons</span><span class="sxs-lookup"><span data-stu-id="7fb60-112">Tone Mapping</span></span>

<span data-ttu-id="7fb60-113">Le placage de ton simule généralement des phénomènes optiques qui ne peuvent pas être provoqués par la récupération d’urgence du moniteur.</span><span class="sxs-lookup"><span data-stu-id="7fb60-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="7fb60-114">Il s’agit, par exemple, de halos ou de la floraison (principalement des propriétés de lentilles), du décalage bleu qui se produit dans l’oeil humain en conditions d’éclairage faible et d’autres adaptations qui résultent de la biochimie de l’oeil.</span><span class="sxs-lookup"><span data-stu-id="7fb60-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="7fb60-115">Si la récupération d’urgence de l’affichage était assez grande, le mappage de tonalité n’est pas si nécessaire, à l’exception de la fourniture d’effets artistiques ou de certaines propriétés d’une lentille d’appareil photo ou d’un appareil à couplage de frais (CCD).</span><span class="sxs-lookup"><span data-stu-id="7fb60-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="7fb60-116">Le placage de tons divise la plage de valeurs de luminance dans une scène en un ensemble de zones.</span><span class="sxs-lookup"><span data-stu-id="7fb60-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="7fb60-117">Chaque zone englobe une plage de valeurs de luminance.</span><span class="sxs-lookup"><span data-stu-id="7fb60-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="7fb60-118">HDR utilise les termes suivants :</span><span class="sxs-lookup"><span data-stu-id="7fb60-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="7fb60-119">Plage de valeurs de luminance dans une zone</span><span class="sxs-lookup"><span data-stu-id="7fb60-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="7fb60-120">Gris moyen-zone de luminosité du milieu de la scène</span><span class="sxs-lookup"><span data-stu-id="7fb60-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="7fb60-121">Taux de plage dynamique de la luminance de scène la plus élevée à la luminance de scène la plus faible</span><span class="sxs-lookup"><span data-stu-id="7fb60-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="7fb60-122">Mesure d’éclairage de scène clé-subjective : elle varie d’un clair à l’obscurité</span><span class="sxs-lookup"><span data-stu-id="7fb60-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="7fb60-123">Pour calculer la luminance à partir des valeurs RVB, utilisez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7fb60-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="7fb60-124">La luminance moyenne des journaux est une approximation utile pour la clé d’une scène.</span><span class="sxs-lookup"><span data-stu-id="7fb60-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="7fb60-125">Une équation générale se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="7fb60-125">A general equation looks like this:</span></span>

<span data-ttu-id="7fb60-126">L<sub>w</sub> = exp \[ 1/N ( \[ Journal Sum (Delta + L<sub>w</sub>(x, y)) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="7fb60-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="7fb60-127">Où :</span><span class="sxs-lookup"><span data-stu-id="7fb60-127">Where:</span></span>

-   <span data-ttu-id="7fb60-128">L<sub>w</sub> -log-luminance moyenne</span><span class="sxs-lookup"><span data-stu-id="7fb60-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="7fb60-129">N-nombre de pixels dans l’image</span><span class="sxs-lookup"><span data-stu-id="7fb60-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="7fb60-130">Delta : petit facteur permettant d’éviter les problèmes avec les pixels noirs</span><span class="sxs-lookup"><span data-stu-id="7fb60-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="7fb60-131">L<sub>w</sub>(x, y)-la luminance de l’espace universel pour le pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="7fb60-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="7fb60-132">Pour le mapper à une valeur de gris moyen, voici un opérateur de mise à l’échelle de luminance :</span><span class="sxs-lookup"><span data-stu-id="7fb60-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="7fb60-133">L (x, y) = a \* l<sub>w</sub>(x, y)/l<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="7fb60-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="7fb60-134">Où :</span><span class="sxs-lookup"><span data-stu-id="7fb60-134">Where:</span></span>

-   <span data-ttu-id="7fb60-135">L (x, y)-luminance à l’échelle pour le pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="7fb60-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="7fb60-136">valeur de clé-image après l’application de la mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="7fb60-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="7fb60-137">Enfin, voici un opérateur de mappage de ton simple pour compresser les luminances élevées :</span><span class="sxs-lookup"><span data-stu-id="7fb60-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="7fb60-138">L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))</span><span class="sxs-lookup"><span data-stu-id="7fb60-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="7fb60-139">Où :</span><span class="sxs-lookup"><span data-stu-id="7fb60-139">Where:</span></span>

-   <span data-ttu-id="7fb60-140">L<sub>(</sub>x, y)-luminance compressée et mise à l’échelle pour le pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="7fb60-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="7fb60-141">valeur de clé-image après l’application de la mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="7fb60-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="7fb60-142">Cet opérateur met à l’échelle les luminances élevées par 1/L et les luminances basses de 1.</span><span class="sxs-lookup"><span data-stu-id="7fb60-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="7fb60-143">Pour plus d’informations, consultez le document suivant.</span><span class="sxs-lookup"><span data-stu-id="7fb60-143">For more details, see the following paper.</span></span>

<span data-ttu-id="7fb60-144">Reinhard, Erik, Mike, Peter Shirley et James Ferwerda.</span><span class="sxs-lookup"><span data-stu-id="7fb60-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="7fb60-145">[« Reproduction des sons photographiques pour les images numériques »](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span><span class="sxs-lookup"><span data-stu-id="7fb60-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="7fb60-146">Transactions ACM sur Graphics (TOG), procédure du 29 Conférence annuelle sur les graphiques informatiques et les techniques interactives (SIGGRAPH), pp. 267-276.</span><span class="sxs-lookup"><span data-stu-id="7fb60-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="7fb60-147">New York, NY : ACM Press, 2002.</span><span class="sxs-lookup"><span data-stu-id="7fb60-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fb60-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7fb60-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb60-149">Rubriques avancées</span><span class="sxs-lookup"><span data-stu-id="7fb60-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 



