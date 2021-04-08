---
title: effet de table de recherche 3D
description: Une table de recherche 3D est un effet à usage général qui est utilisé pour encapsuler n’importe quel effet d’image 1 1 en précalculant la façon dont l’effet mappe les entrées aux sorties pour un sous-ensemble de toutes les valeurs d’entrée.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844425"
---
# <a name="3d-lookup-table-effect"></a><span data-ttu-id="2227b-103">effet de table de recherche 3D</span><span class="sxs-lookup"><span data-stu-id="2227b-103">3D lookup table effect</span></span>

<span data-ttu-id="2227b-104">Une table de recherche 3D est un effet à usage général qui est utilisé pour encapsuler n’importe quel effet d’image 1:1 en précalculant la façon dont l’effet mappe les entrées aux sorties pour un sous-ensemble de toutes les valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2227b-104">A 3D look-up table is a general-purpose effect that is used to encapsulate any 1:1 imaging effect by pre-computing how the effect maps inputs to outputs for a subset of all input values.</span></span>

<span data-ttu-id="2227b-105">L’effet de la table de recherche 3D (LUT) modifie une image d’entrée à l’aide de la valeur de couleur RVB de l’image pour indexer une texture 3D, où la texture contient une valeur de sortie précalculée d’un pipeline d’effet arbitraire.</span><span class="sxs-lookup"><span data-stu-id="2227b-105">The 3D Lookup Table (LUT) effect modifies an input image by using the image's RGB color value to index a 3D texture, where the texture contains a precomputed output value of an arbitrary effect pipeline.</span></span>

<span data-ttu-id="2227b-106">Le LUT 3D doit être chargé dans une ressource de texture GPU afin d’être rendu, ce qui peut être coûteux en fonction de la taille de la texture et des fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2227b-106">The 3D LUT must be loaded into a GPU texture resource in order to be rendered, and this can be expensive depending on the size of the texture and the device capabilities.</span></span> <span data-ttu-id="2227b-107">Les développeurs d’applications peuvent spécifier le moment auquel payer ce coût à l’aide de la ressource D2D [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) .</span><span class="sxs-lookup"><span data-stu-id="2227b-107">Application developers can specify when to pay this cost using the [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D resource.</span></span> <span data-ttu-id="2227b-108">**ID2D1LookupTable3D** a les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="2227b-108">**ID2D1LookupTable3D** has the following attributes:</span></span>

-   <span data-ttu-id="2227b-109">Fournit une représentation abstraite de la ressource GPU de l’un des graphiques 3D.</span><span class="sxs-lookup"><span data-stu-id="2227b-109">Provides an abstracted representation of 3D LUT's GPU resource.</span></span>
-   <span data-ttu-id="2227b-110">Selon les fonctionnalités de l’appareil, une texture 2D ou 3D est créée et remplie avec les données LUT fournies.</span><span class="sxs-lookup"><span data-stu-id="2227b-110">Depending on the device capabilities, either a 2D or 3D texture will be created and filled with the provided LUT data.</span></span>
-   <span data-ttu-id="2227b-111">Peut être passé à la propriété de l’effet de LUT 3D pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="2227b-111">Can be passed to the 3D LUT effect's property for rendering.</span></span>

<span data-ttu-id="2227b-112">Le CLSID de cet effet est CLSID \_ D2D1LookupTable3D.</span><span class="sxs-lookup"><span data-stu-id="2227b-112">The CLSID for this effect is CLSID\_D2D1LookupTable3D.</span></span>

-   [<span data-ttu-id="2227b-113">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="2227b-113">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="2227b-114">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="2227b-114">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="2227b-115">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="2227b-115">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="2227b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2227b-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2227b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2227b-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="2227b-118">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="2227b-118">Example image</span></span>

![exemple de sortie d’effet](images/3dlookuptable-effect.png)

## <a name="sample-code"></a><span data-ttu-id="2227b-120">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="2227b-120">Sample code</span></span>

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a><span data-ttu-id="2227b-121">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="2227b-121">Effect properties</span></span>

<span data-ttu-id="2227b-122">Les propriétés de l’effet de table de recherche 3D sont définies par l’énumération [**d2d1 \_ LOOKUPTABLE3D \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) .</span><span class="sxs-lookup"><span data-stu-id="2227b-122">The properties for the 3D lookup table effect are defined by the [**D2D1\_LOOKUPTABLE3D\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2227b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2227b-123">Requirements</span></span>



| <span data-ttu-id="2227b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2227b-124">Requirement</span></span> | <span data-ttu-id="2227b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2227b-125">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="2227b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2227b-126">Minimum supported client</span></span> | <span data-ttu-id="2227b-127">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2227b-127">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2227b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2227b-128">Minimum supported server</span></span> | <span data-ttu-id="2227b-129">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2227b-129">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2227b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="2227b-130">Header</span></span>                   | <span data-ttu-id="2227b-131">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="2227b-131">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="2227b-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2227b-132">Library</span></span>                  | <span data-ttu-id="2227b-133">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2227b-133">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="2227b-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2227b-134">Related topics</span></span>

* [<span data-ttu-id="2227b-135">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="2227b-135">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
