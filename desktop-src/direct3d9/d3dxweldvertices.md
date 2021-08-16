---
description: Les soudures ensemble des vertex répliqués ayant des attributs identiques. Cette méthode utilise des valeurs epsilon spécifiées pour les comparaisons d’égalité.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: D3DXWeldVertices, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6a9a05573467e0725785a6272e5542c4f871080fe221ac12078b17165eb5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803272"
---
# <a name="d3dxweldvertices-function"></a>D3DXWeldVertices fonction)

Les soudures ensemble des vertex répliqués ayant des attributs identiques. Cette méthode utilise des valeurs epsilon spécifiées pour les comparaisons d’égalité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un objet [**ID3DXMesh**](id3dxmesh.md) , le maillage à partir duquel les vertex de soudure.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs à partir de [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*pEpsilons* \[ dans\]
</dt> <dd>

Type : **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Pointeur vers une structure [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , en spécifiant les valeurs epsilon à utiliser pour cette méthode. Utilisez **null** pour initialiser tous les membres de la structure avec une valeur par défaut de 1,0 e-6F.

</dd> <dt>

*pAdjacencyIn* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage source. Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF. Si ce paramètre a la valeur **null**, [**ID3DXBaseMesh :: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) est appelé pour créer des informations d’adjacence logiques.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage optimisé. Si le bord n’a pas de faces adjacentes, la valeur est 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Tableau de DWORDs, un par visage, qui identifie la face d’origine du maillage qui correspond à chaque visage dans le maillage soudé.

</dd> <dt>

*ppVertexRemap* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex. Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction utilise les informations d’adjacence fournies pour déterminer les points répliqués. Les vertex sont fusionnés en fonction d’une comparaison Epsilon. Les vertex avec la même position doivent déjà avoir été calculés et représentés par des données représentatives du point.

Cette fonction combine des vertex soudés logiquement qui ont des composants similaires, tels que des normales ou des coordonnées de texture dans pEpsilons.

L’exemple de code suivant appelle cette fonction avec le soudage activé. Les vertex sont comparés à l’aide des valeurs epsilon pour le vecteur normal et la position du vertex. Un pointeur est retourné à un tableau de remappages de visages (*pFaceRemap*).


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
