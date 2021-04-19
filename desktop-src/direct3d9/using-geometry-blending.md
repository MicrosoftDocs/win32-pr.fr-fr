---
description: La structure définie par l’utilisateur suivante peut être utilisée pour les vertex qui seront mélangés entre deux matrices.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Utilisation de la fusion géométrique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544540"
---
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="01ffb-103">Utilisation de la fusion géométrique (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="01ffb-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="01ffb-104">La structure définie par l’utilisateur suivante peut être utilisée pour les vertex qui seront mélangés entre deux matrices.</span><span class="sxs-lookup"><span data-stu-id="01ffb-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



<span data-ttu-id="01ffb-105">Le poids de fusion doit apparaître après les données position et RHW dans le prix de la Commission et avant la normale du vertex.</span><span class="sxs-lookup"><span data-stu-id="01ffb-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="01ffb-106">Notez que le format de vertex précédent contient une seule valeur de poids de fusion.</span><span class="sxs-lookup"><span data-stu-id="01ffb-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="01ffb-107">Cela est dû au fait qu’il y aura deux matrices universelles définies dans les États [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) et **D3DTS \_ WORLDMATRIX**(1) Transform.</span><span class="sxs-lookup"><span data-stu-id="01ffb-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="01ffb-108">Le système fusionne chaque vertex entre ces deux matrices à l’aide de la valeur de poids unique.</span><span class="sxs-lookup"><span data-stu-id="01ffb-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="01ffb-109">Pour trois matrices, seuls deux poids sont requis, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="01ffb-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="01ffb-110">La définition des poids de la peau est simple.</span><span class="sxs-lookup"><span data-stu-id="01ffb-110">Defining skin weights is easy.</span></span> <span data-ttu-id="01ffb-111">L’utilisation d’une fonction linéaire de la distance entre les jointures est un bon début, mais une fonction sigmoïde plus lisse semble mieux.</span><span class="sxs-lookup"><span data-stu-id="01ffb-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="01ffb-112">Le choix d’une fonction de distribution de poids d’épiderme peut entraîner des froissures nets au niveau des jointures, si nécessaire, en utilisant une variation importante du poids de la peau sur une distance.</span><span class="sxs-lookup"><span data-stu-id="01ffb-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="01ffb-113">Définition des matrices de fusion</span><span class="sxs-lookup"><span data-stu-id="01ffb-113">Setting Blending Matrices</span></span>

<span data-ttu-id="01ffb-114">Vous définissez les matrices de transformation entre lesquelles le système fusionne en appelant la méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="01ffb-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="01ffb-115">Définissez le premier paramètre sur une valeur définie par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , puis définissez le deuxième paramètre sur l’adresse de la matrice à définir.</span><span class="sxs-lookup"><span data-stu-id="01ffb-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="01ffb-116">L’exemple de code C++ suivant définit deux matrices universelles, entre lesquelles la géométrie est mélangée pour créer l’illusion d’un bras joint.</span><span class="sxs-lookup"><span data-stu-id="01ffb-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



<span data-ttu-id="01ffb-117">La définition d’une matrice de fusion fait simplement en sorte que le système met en cache la matrice pour une utilisation ultérieure ; elle n’indique pas au système de commencer à fusionner les vertex.</span><span class="sxs-lookup"><span data-stu-id="01ffb-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="01ffb-118">Activation de la fusion de géométrie</span><span class="sxs-lookup"><span data-stu-id="01ffb-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="01ffb-119">La fusion géométrique est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="01ffb-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="01ffb-120">Pour activer la fusion de géométrie, appelez la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) pour définir l' \_ État de rendu D3DRS VERTEXBLEND sur une valeur du type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="01ffb-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="01ffb-121">L’exemple de code suivant montre ce à quoi peut ressembler cet appel lors de la définition de l’état de rendu d’une fusion entre deux matrices universelles.</span><span class="sxs-lookup"><span data-stu-id="01ffb-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="01ffb-122">Lorsque D3DRS \_ VERTEXBLEND est défini sur une valeur autre que D3DVBF \_ Disable, le système suppose que le nombre approprié de poids de fusion est inclus dans le format de vertex.</span><span class="sxs-lookup"><span data-stu-id="01ffb-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="01ffb-123">Il vous incombe de fournir un format de vertex conforme et de fournir une description appropriée de ce format aux méthodes de rendu Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01ffb-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="01ffb-124">Lorsqu’il est activé, le système effectue une fusion géométrique pour tous les objets rendus par les méthodes de rendu DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="01ffb-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="01ffb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01ffb-125">See Also</span></span>

[<span data-ttu-id="01ffb-126">Correction des codes de fonction de la Commission (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="01ffb-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="01ffb-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01ffb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01ffb-128">Fusion géométrique</span><span class="sxs-lookup"><span data-stu-id="01ffb-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 
