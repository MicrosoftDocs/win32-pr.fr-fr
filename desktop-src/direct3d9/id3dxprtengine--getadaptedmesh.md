---
description: Retourne un maillage avec les modifications résultant de l’échantillonnage spatial adaptatif. Le maillage retourné contient uniquement des positions, des normales et des coordonnées de texture (s’il est défini).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine :: GetAdaptedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e38937628bc36f49059bcb3e798a6d13e538c572c1c5fb6ef20865ed05385d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747669"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>ID3DXPRTEngine :: GetAdaptedMesh, méthode

Retourne un maillage avec les modifications résultant de l’échantillonnage spatial adaptatif. Le maillage retourné contient uniquement des positions, des normales et des coordonnées de texture (s’il est défini).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers un appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé pour créer le maillage de sortie.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers la face de maille d’origine qui a été fractionnée pour générer la face actuelle.

</dd> <dt>

*pVertRemap* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de destination contenant les trois vertex de maillage d’origine qui sont les parents du vertex actuel.

</dd> <dt>

*pfVertWeights* \[ in, out\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau de destination contenant des facteurs de fusion pour les vertex pVertRemap.

</dd> <dt>

*ppMesh* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***

Pointeur vers l’objet de maillage [**ID3DXMesh**](id3dxmesh.md) de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Remarques

pVertRemap et pfVertWeights peuvent être utilisés pour interpoler toute valeur par vertex sur la maille.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
