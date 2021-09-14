---
description: 'ID3DX10Mesh :: Optimize, méthode-génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.'
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'ID3DX10Mesh :: Optimize, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f530995a2388d3ec2627ac5ce128271ed085a779
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228221"
---
# <a name="id3dx10meshoptimize-method"></a>ID3DX10Mesh :: Optimize, méthode

Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Spécifie le type d’optimisation à effectuer. Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs de D3DXMESHOPT et D3DXMESH (à l’exception de D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly et D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pFaceRemap* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Tableau de UINTs, un par visage, qui identifie la facette d’origine qui correspond à chaque visage dans le maillage optimisé. Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.

</dd> <dt>

*ppVertexRemap* \[ à\]
</dt> <dd>

Type : **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Adresse d’un pointeur vers une [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex. Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Cette méthode génère un nouveau maillage. Avant d’exécuter Optimize, une application doit générer une mémoire tampon de contiguïté en appelant [**ID3DX10Mesh :: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md). La mémoire tampon d’adjacence contient des données d’contiguïté, telles qu’une liste de bords et les faces adjacentes les unes aux autres.

Cette méthode est très similaire à la méthode [**ID3DX10Mesh :: CloneMesh**](id3dx10mesh-clonemesh.md) , à ceci près qu’elle peut effectuer une optimisation lors de la génération du nouveau clone de la maille. Le maillage de sortie hérite de tous les paramètres de création du maillage d’entrée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
