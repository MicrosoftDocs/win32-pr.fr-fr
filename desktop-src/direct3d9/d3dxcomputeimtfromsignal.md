---
description: Calcule les IMTs par triangle à partir d’un signal spécifié par l’application, qui varie en fonction de la surface du maillage (généralement à une fréquence plus élevée que les données de vertex). Le signal est évalué par le biais d’une fonction de rappel spécifiée par l’utilisateur.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: D3DXComputeIMTFromSignal, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538344"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>D3DXComputeIMTFromSignal fonction)

Calcule les IMTs par triangle à partir d’un signal spécifié par l’application, qui varie en fonction de la surface du maillage (généralement à une fréquence plus élevée que les données de vertex). Le signal est évalué par le biais d’une fonction de rappel spécifiée par l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.

</dd> <dt>

*dwTextureIndex* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.

</dd> <dt>

*uSignalDimension* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de composants dans chaque point de données dans le signal.

</dd> <dt>

*fMaxUVDistance* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Distance maximale entre les vertex ; l’algorithme continue à se subdiviser jusqu’à ce que la distance entre tous les vertex soit inférieure ou égale à fMaxUVDistance.

</dd> <dt>

*dwOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Options de retour à la ligne. Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pSignalCallback* \[ dans\]
</dt> <dd>

Type : **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de signal à des coordonnées U, V arbitraires. La fonction suit le prototype de [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).

</dd> <dt>

*pUserData* \[ dans\]
</dt> <dd>

Type : **void \***

Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel de signal. Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État. Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

</dd> <dt>

*ppIMTData* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné. Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Cette fonction requiert que le maillage d’entrée contienne un mappage de texture signal-à-maillage (coordonnées de texture). Elle permet à l’utilisateur de définir un signal arbitrairement sur la surface de la maille.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[UVAtlas, fonctions](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Utilisation de UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
