---
description: Utilisation d’une couleur RVB 16 bits
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Utilisation d’une couleur RVB 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518316"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="50818-103">Utilisation d’une couleur RVB 16 bits</span><span class="sxs-lookup"><span data-stu-id="50818-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="50818-104">Deux formats sont définis pour la couleur RVB non compressée 16 bits :</span><span class="sxs-lookup"><span data-stu-id="50818-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="50818-105">MEDIASUBTYPE \_ 555 utilise cinq bits pour chaque composant rouge, vert et bleu d’un pixel.</span><span class="sxs-lookup"><span data-stu-id="50818-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="50818-106">Le bit le plus significatif dans le **mot** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="50818-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="50818-107">MEDIASUBTYPE \_ 565 utilise cinq bits pour les composants rouge et bleu, et six bits pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="50818-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="50818-108">Ce format reflète le fait que la vision humaine est la plus sensible aux parties vertes du spectre visible.</span><span class="sxs-lookup"><span data-stu-id="50818-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="50818-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="50818-109">**RGB 565**</span></span>

<span data-ttu-id="50818-110">Pour extraire les composants de couleur d’une image RVB 565, traitez chaque pixel comme un type de **mot** et utilisez les masques de bits suivants :</span><span class="sxs-lookup"><span data-stu-id="50818-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="50818-111">Récupérez les composants de couleur d’un pixel comme suit :</span><span class="sxs-lookup"><span data-stu-id="50818-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="50818-112">N’oubliez pas que les canaux rouge et bleu sont 5 bits et que le canal vert est 6 bits.</span><span class="sxs-lookup"><span data-stu-id="50818-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="50818-113">Pour convertir ces valeurs en composants 8 bits (pour les couleurs RVB 24 bits ou 32 bits), vous devez déplacer le nombre de bits approprié vers la gauche :</span><span class="sxs-lookup"><span data-stu-id="50818-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="50818-114">Inversez ce processus pour créer un pixel RVB 565.</span><span class="sxs-lookup"><span data-stu-id="50818-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="50818-115">En supposant que les valeurs de couleur ont été tronquées avec le nombre correct de bits :</span><span class="sxs-lookup"><span data-stu-id="50818-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="50818-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="50818-116">**RGB 555**</span></span>

<span data-ttu-id="50818-117">L’utilisation de RGB 555 est fondamentalement identique à la couleur RVB 565, sauf que les masques de bits et les opérations de décalage de bits sont différents.</span><span class="sxs-lookup"><span data-stu-id="50818-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="50818-118">Pour récupérer les composants de couleur à partir d’un pixel RVB 555, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="50818-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="50818-119">Pour empaqueter les valeurs de couleur rouge, vert et bleu dans un pixel RVB 555, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="50818-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="50818-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50818-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50818-121">Sous-types de vidéos RVB non compressés</span><span class="sxs-lookup"><span data-stu-id="50818-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



