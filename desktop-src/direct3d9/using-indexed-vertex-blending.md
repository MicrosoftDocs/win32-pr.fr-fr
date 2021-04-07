---
description: Les États de transformation 256-511 sont réservés pour stocker jusqu’à 256 matrices qui peuvent être indexées à l’aide d’indices 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Utilisation de la fusion de vertex indexée (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845957"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="d9536-103">Utilisation de la fusion de vertex indexée (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9536-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="d9536-104">Les États de transformation 256-511 sont réservés pour stocker jusqu’à 256 matrices qui peuvent être indexées à l’aide d’indices 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d9536-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="d9536-105">Utilisez la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) pour mapper les index 0-255 aux États de transformation correspondants.</span><span class="sxs-lookup"><span data-stu-id="d9536-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="d9536-106">L’exemple de code suivant montre comment utiliser la méthode [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) pour définir la matrice à l’état de transformation numéro 256 sur une matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="d9536-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="d9536-107">Pour activer ou désactiver la fusion des vertex indexés, affectez \_ à l’état de rendu D3DRS INDEXEDVERTEXBLENDENABLE la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="d9536-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="d9536-108">Lorsque l’état de rendu est activé, vous devez passer les index de matrice comme des DWORDs compressés avec chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="d9536-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="d9536-109">Lorsque cet état de rendu est désactivé et que la fusion de vertex est activée, cela équivaut à avoir les index de matrice 0, 1, 2 et 3 dans chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="d9536-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="d9536-110">L’exemple de code ci-dessous utilise la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) pour activer la fusion des vertex indexés.</span><span class="sxs-lookup"><span data-stu-id="d9536-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="d9536-111">Pour activer ou désactiver la fusion de vertex, définissez l’état de rendu [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) sur une valeur autre que D3DRS \_ Disable à partir du type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="d9536-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="d9536-112">Si cet état de rendu n’a pas la valeur D3DRS \_ Disable, vous devez passer le nombre requis de poids pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="d9536-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="d9536-113">L’exemple de code suivant utilise **IDirect3DDevice9 :: SetRenderState** pour activer la fusion de vertex avec trois pondérations pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="d9536-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="d9536-114">Détermination de la prise en charge de la fusion des vertex indexés</span><span class="sxs-lookup"><span data-stu-id="d9536-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="d9536-115">Pour déterminer la taille maximale de la matrice de fusion des vertex indexés, vérifiez le membre MaxVertexBlendMatrixIndex de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="d9536-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="d9536-116">L’exemple de code ci-dessous utilise la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) pour récupérer cette taille.</span><span class="sxs-lookup"><span data-stu-id="d9536-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="d9536-117">Si la valeur définie dans MaxVertexBlendMatrixIndex est 0, l’appareil ne prend pas en charge les matrices indexées.</span><span class="sxs-lookup"><span data-stu-id="d9536-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="d9536-118">Lorsque le traitement du vertex logiciel est utilisé, 256 matrices peuvent être utilisées pour la fusion de vertex indexée, avec ou sans fusion normale.</span><span class="sxs-lookup"><span data-stu-id="d9536-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="d9536-119">Passage d’index de matrice à Direct3D</span><span class="sxs-lookup"><span data-stu-id="d9536-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="d9536-120">Les index de la matrice universelle peuvent être passés à Direct3D à l’aide des nuanceurs de vertex hérités-Commission des points de suivi ou déclarations.</span><span class="sxs-lookup"><span data-stu-id="d9536-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="d9536-121">L’exemple de code ci-dessous montre comment utiliser les nuanceurs vertex hérités.</span><span class="sxs-lookup"><span data-stu-id="d9536-121">The code example below shows how to use legacy vertex shaders.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



<span data-ttu-id="d9536-122">Lorsqu’un nuanceur de sommets hérité est utilisé, les index de matrice sont passés avec des positions de vertex à l’aide d' \_ indicateurs D3DFVF XYZBn.</span><span class="sxs-lookup"><span data-stu-id="d9536-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="d9536-123">Les index de matrice sont passés comme octets à l’intérieur d’une valeur DWORD et doivent être présents immédiatement après le dernier poids de vertex.</span><span class="sxs-lookup"><span data-stu-id="d9536-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="d9536-124">Les poids des vertex sont également passés à l’aide de D3DFVF \_ XYZBn.</span><span class="sxs-lookup"><span data-stu-id="d9536-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="d9536-125">Une valeur DWORD compressée contient index3, index2, index1 et index0, où index0 se trouve dans l’octet le plus bas de la valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="d9536-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="d9536-126">Le nombre d’index de la matrice mondiale utilisé est égal au nombre passé au nombre de matrices utilisées pour la fusion comme défini par [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="d9536-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="d9536-127">Lorsqu’une déclaration est utilisée, D3DVSDE \_ BLENDINDICES définit le registre de vertex d’entrée à partir duquel obtenir les index de matrice.</span><span class="sxs-lookup"><span data-stu-id="d9536-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="d9536-128">Les index de matrice doivent être passés en tant que D3DVSDT \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d9536-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="d9536-129">L’exemple de code ci-dessous montre comment utiliser les déclarations.</span><span class="sxs-lookup"><span data-stu-id="d9536-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="d9536-130">Notez que l’ordre des composants n’est plus important, sauf en utilisant un nuanceur de sommets à fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="d9536-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="d9536-131">Voici la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="d9536-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="d9536-132">Voici la déclaration Register correspondante.</span><span class="sxs-lookup"><span data-stu-id="d9536-132">Here is the corresponding register declaration.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a><span data-ttu-id="d9536-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9536-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9536-134">Fusion des vertex indexés</span><span class="sxs-lookup"><span data-stu-id="d9536-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
