---
description: Effectuez des dépassements de logiciels sur un tableau de vertex.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: ID3DX10SkinInfo ::D méthode oSoftwareSkinning (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535178"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo ::D méthode oSoftwareSkinning

Effectuez des dépassements de logiciels sur un tableau de vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartVertex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de base 0 dans pSrcVertices.

</dd> <dt>

*VertexCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex à transformer.

</dd> <dt>

*pSrcVertices* \[ dans\]
</dt> <dd>

Type : **void \***

Pointeur vers un tableau de vertex à transformer.

</dd> <dt>

*SrcStride* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Taille, en octets, d’un vertex dans pSrcVertices.

</dd> <dt>

*pDestVertices* \[ in, out\]
</dt> <dd>

Type : **void \***

Pointeur vers un tableau de vertex, qui sera rempli avec les vertex transformés.

</dd> <dt>

*DestStride* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Taille, en octets, d’un vertex dans pDestVertices.

</dd> <dt>

*pBoneMatrices* \[ dans\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Tableau de matrices qui sera utilisé pour transformer les points mappés à chaque segment, de telle sorte que les vertex mappés au segment \[ \] sont transformés par pBoneMatrices \[ i \] . Ce tableau sera utilisé pour transformer les matrices uniquement si la valeur IsNormal dans pChannelDescs est définie sur **false**, sinon pInverseTransposeBoneMatrices sera utilisé.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ dans\]
</dt> <dd>

Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Si cette valeur est **null**, elle sera définie sur pBoneMatrices. Ce tableau de matrices sera utilisé pour transformer les vertex uniquement si la valeur IsNormal dans pChannelDescs est définie sur **true**, sinon pBoneMatrices sera utilisé.

</dd> <dt>

*pChannelDescs* \[ dans\]
</dt> <dd>

Type : d3dx10 de l' **[ **\_ apparence du \_ canal**](d3dx10-skinning-channel.md)\***

Pointeur vers une \_ structure de canal d’apparence d3dx10 \_ , qui détermine le membre du vertex decl sur lequel le détourage de logiciel sera effectué.

</dd> <dt>

*NumChannels* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de structures de \_ canal d’apparence d3dx10 \_ dans pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG.

## <a name="remarks"></a>Notes

Voici un exemple d’utilisation de l’application de pelures de logiciels :


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
