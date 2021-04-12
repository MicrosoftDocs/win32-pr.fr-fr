---
description: Définit une couleur matérielle de base qui peut être appliquée à un maillage complet ou à des visages individuels d’un maillage. La puissance est l’exposant spéculaire du matériau.
ms.assetid: vs|directx_sdk|~\material.htm
title: Matériau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480704"
---
# <a name="material"></a><span data-ttu-id="4976c-104">Matériau</span><span class="sxs-lookup"><span data-stu-id="4976c-104">Material</span></span>

<span data-ttu-id="4976c-105">Définit une couleur matérielle de base qui peut être appliquée à un maillage complet ou à des visages individuels d’un maillage.</span><span class="sxs-lookup"><span data-stu-id="4976c-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="4976c-106">La puissance est l’exposant spéculaire du matériau.</span><span class="sxs-lookup"><span data-stu-id="4976c-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="4976c-107">Où :</span><span class="sxs-lookup"><span data-stu-id="4976c-107">Where:</span></span>

-   <span data-ttu-id="4976c-108">faceColor : couleur de face.</span><span class="sxs-lookup"><span data-stu-id="4976c-108">faceColor - Face color.</span></span> <span data-ttu-id="4976c-109">Modèle ColorRGBA.</span><span class="sxs-lookup"><span data-stu-id="4976c-109">A ColorRGBA template.</span></span> <span data-ttu-id="4976c-110">Consultez [**ColorRGBA**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="4976c-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="4976c-111">exposant de couleur spéculaire de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4976c-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="4976c-112">specularColor : couleur spéculaire.</span><span class="sxs-lookup"><span data-stu-id="4976c-112">specularColor - Material specular color.</span></span> <span data-ttu-id="4976c-113">Modèle ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="4976c-113">A ColorRGB template.</span></span> <span data-ttu-id="4976c-114">Consultez [**ColorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="4976c-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="4976c-115">emissiveColor : couleur de matériau émissif.</span><span class="sxs-lookup"><span data-stu-id="4976c-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="4976c-116">Modèle ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="4976c-116">A ColorRGB template.</span></span> <span data-ttu-id="4976c-117">Consultez [**ColorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="4976c-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="4976c-118">La couleur ambiante requiert un composant alpha.</span><span class="sxs-lookup"><span data-stu-id="4976c-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="4976c-119">[**TextureFilename**](texturefilename.md) est un objet de données facultatif.</span><span class="sxs-lookup"><span data-stu-id="4976c-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="4976c-120">Si cet objet n’est pas présent, la face n’est pas texturée.</span><span class="sxs-lookup"><span data-stu-id="4976c-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="4976c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4976c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4976c-122">Modèles</span><span class="sxs-lookup"><span data-stu-id="4976c-122">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



