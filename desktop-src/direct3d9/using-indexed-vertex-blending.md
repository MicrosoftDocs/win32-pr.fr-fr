---
description: Les États de transformation 256-511 sont réservés pour stocker jusqu’à 256 matrices qui peuvent être indexées à l’aide d’indices 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Utilisation de la fusion de vertex indexée (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2d14e66fd934e2eaa8b403d694d203edddb229aab0795fa4a396b8baf367ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519474"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Utilisation de la fusion de vertex indexée (Direct3D 9)

Les États de transformation 256-511 sont réservés pour stocker jusqu’à 256 matrices qui peuvent être indexées à l’aide d’indices 8 bits. Utilisez la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) pour mapper les index 0-255 aux États de transformation correspondants. L’exemple de code suivant montre comment utiliser la méthode [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) pour définir la matrice à l’état de transformation numéro 256 sur une matrice d’identité.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Pour activer ou désactiver la fusion des vertex indexés, affectez \_ à l’état de rendu D3DRS INDEXEDVERTEXBLENDENABLE la **valeur true**. Lorsque l’état de rendu est activé, vous devez passer les index de matrice comme des DWORDs compressés avec chaque vertex. Lorsque cet état de rendu est désactivé et que la fusion de vertex est activée, cela équivaut à avoir les index de matrice 0, 1, 2 et 3 dans chaque vertex. L’exemple de code ci-dessous utilise la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) pour activer la fusion des vertex indexés.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Pour activer ou désactiver la fusion de vertex, définissez l’état de rendu [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) sur une valeur autre que D3DRS \_ Disable à partir du type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Si cet état de rendu n’a pas la valeur D3DRS \_ Disable, vous devez passer le nombre requis de poids pour chaque vertex. L’exemple de code suivant utilise **IDirect3DDevice9 :: SetRenderState** pour activer la fusion de vertex avec trois pondérations pour chaque vertex.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Détermination de la prise en charge de la fusion des vertex indexés

Pour déterminer la taille maximale de la matrice de fusion des vertex indexés, vérifiez le membre MaxVertexBlendMatrixIndex de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . L’exemple de code ci-dessous utilise la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) pour récupérer cette taille.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Si la valeur définie dans MaxVertexBlendMatrixIndex est 0, l’appareil ne prend pas en charge les matrices indexées.

> [!Note]  
> Lorsque le traitement du vertex logiciel est utilisé, 256 matrices peuvent être utilisées pour la fusion de vertex indexée, avec ou sans fusion normale.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Passage d’index de matrice à Direct3D

Les index de la matrice universelle peuvent être passés à Direct3D à l’aide des nuanceurs de vertex hérités-Commission des points de suivi ou déclarations.

L’exemple de code ci-dessous montre comment utiliser les nuanceurs vertex hérités.


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



Lorsqu’un nuanceur de sommets hérité est utilisé, les index de matrice sont passés avec des positions de vertex à l’aide d' \_ indicateurs D3DFVF XYZBn. Les index de matrice sont passés comme octets à l’intérieur d’une valeur DWORD et doivent être présents immédiatement après le dernier poids de vertex. Les poids des vertex sont également passés à l’aide de D3DFVF \_ XYZBn. Une valeur DWORD compressée contient index3, index2, index1 et index0, où index0 se trouve dans l’octet le plus bas de la valeur DWORD. Le nombre d’index de la matrice mondiale utilisé est égal au nombre passé au nombre de matrices utilisées pour la fusion comme défini par [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).

Lorsqu’une déclaration est utilisée, D3DVSDE \_ BLENDINDICES définit le registre de vertex d’entrée à partir duquel obtenir les index de matrice. Les index de matrice doivent être passés en tant que D3DVSDT \_ UBYTE4.

L’exemple de code ci-dessous montre comment utiliser les déclarations. Notez que l’ordre des composants n’est plus important, sauf en utilisant un nuanceur de sommets à fonction fixe.

Voici la déclaration de vertex.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Voici la déclaration Register correspondante.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion des vertex indexés](indexed-vertex-blending.md)
</dt> </dl>

 

 
