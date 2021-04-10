---
description: Dans Direct3D, toutes les images à deux dimensions (2D) sont représentées par une plage linéaire de mémoire appelée surface.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formats de surface (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109375"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="0da03-103">Formats de surface (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0da03-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="0da03-104">Dans Direct3D, toutes les images à deux dimensions (2D) sont représentées par une plage linéaire de mémoire appelée surface.</span><span class="sxs-lookup"><span data-stu-id="0da03-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="0da03-105">Une surface peut être considérée comme un tableau 2D où chaque élément contient une valeur de couleur représentant une petite section de l’image, appelée pixel.</span><span class="sxs-lookup"><span data-stu-id="0da03-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="0da03-106">Le niveau de détail d’une image est défini à la fois par le nombre de pixels nécessaires pour représenter l’image et par le nombre de bits nécessaires pour le spectre des couleurs de l’image.</span><span class="sxs-lookup"><span data-stu-id="0da03-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="0da03-107">Par exemple, une image de 800 pixels de large par 600 pixels de haut avec 32 bits de couleur pour chaque pixel (écrit comme 800x600x32) sera plus détaillée qu’une image de 640 pixels de large par 480 pixels de hauteur avec 16 bits de couleur pour chaque pixel (écrit comme 640x480x16).</span><span class="sxs-lookup"><span data-stu-id="0da03-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="0da03-108">De même, l’image plus détaillée nécessitera une surface plus importante pour stocker les données.</span><span class="sxs-lookup"><span data-stu-id="0da03-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="0da03-109">Pour une image 800x600x32, les dimensions du tableau de la surface seront de 800x600, et chaque élément contiendra une valeur 32 bits pour représenter sa couleur.</span><span class="sxs-lookup"><span data-stu-id="0da03-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="0da03-110">Toutes les surfaces ont une taille et stockent un nombre spécifique de bits représentant la couleur.</span><span class="sxs-lookup"><span data-stu-id="0da03-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="0da03-111">Les bits qui représentent la couleur sont séparés en éléments de couleur individuels : rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="0da03-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="0da03-112">Dans Direct3D, tous les éléments de couleur sont définis par le type énuméré [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="0da03-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="0da03-113">Un format de couleur Direct3D est divisé en nombre d’octets réservés pour chaque couleur.</span><span class="sxs-lookup"><span data-stu-id="0da03-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="0da03-114">Par exemple, un format de couleur de 16 bits dans Direct3D est défini en tant que D3DFMT \_ R5G6B5, où 5 bits sont réservés pour le rouge (R), 6 bits pour le vert (G) et 5 bits pour le bleu (B).</span><span class="sxs-lookup"><span data-stu-id="0da03-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0da03-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0da03-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da03-116">Surfaces Direct3D</span><span class="sxs-lookup"><span data-stu-id="0da03-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



