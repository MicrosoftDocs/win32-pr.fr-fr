---
description: Une carte de relief est un objet IDirect3DTexture9 qui utilise un format de pixel spécialisé.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formats de pixel de la carte de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033749"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="fc722-103">Formats de pixel de la carte de relief (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc722-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="fc722-104">Une carte de relief est un objet [**IDirect3DTexture9**](/windows/desktop/api) qui utilise un format de pixel spécialisé.</span><span class="sxs-lookup"><span data-stu-id="fc722-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="fc722-105">Au lieu de stocker les composants de couleur rouge, vert et bleu, chaque pixel d’une carte de relief stocke les valeurs Delta pour vous et v (D<sub>U</sub> et d<sub>v</sub>) et parfois un composant de luminance, L. Ces valeurs sont appliquées par le système, comme décrit dans la rubrique [formules de mappage de relief (Direct3D 9)](bump-mapping-formulas.md) .</span><span class="sxs-lookup"><span data-stu-id="fc722-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="fc722-106">Vous pouvez spécifier un format de pixel de la carte de relief en définissant le format sur l’un des éléments suivants : D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 ou D3DFMT V16U16 \_ .</span><span class="sxs-lookup"><span data-stu-id="fc722-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="fc722-107">Pour obtenir des descriptions, consultez [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="fc722-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="fc722-108">Les composants D<sub>U</sub> et d<sub>V</sub> d’un pixel sont des valeurs signées comprises entre-1,0 et + 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc722-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="fc722-109">Le composant luminance, lorsqu’il est utilisé, est une valeur entière non signée comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="fc722-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="fc722-110">Avant de choisir un format de pixel de placage de relief, vérifiez si le format particulier est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc722-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="fc722-111">Pour plus d’informations, consultez [utilisation du mappage de relief (Direct3D 9)](using-bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="fc722-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fc722-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc722-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc722-113">Placage de relief</span><span class="sxs-lookup"><span data-stu-id="fc722-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



