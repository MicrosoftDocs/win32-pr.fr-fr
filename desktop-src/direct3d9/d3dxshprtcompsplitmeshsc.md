---
description: Utilisé avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé.
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: D3DXSHPRTCompSplitMeshSC, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394099"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>D3DXSHPRTCompSplitMeshSC fonction)

Utilisé avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé. Une fois [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) appelé, cette fonction peut être utilisée pour fractionner le maillage en un groupe de faces/vertex par Super cluster. Chaque supercluster contient tous les visages qui contiennent des vertex classés dans l’un de ses clusters. Tous les vertex connectés à cet ensemble de visages sont également inclus dans le tableau retourné ppVertStatus indiquant si le vertex appartient au Super cluster.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pClusterIDs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

ID de cluster *NumVertices* (extraits d’une mémoire tampon compressée.)

</dd> <dt>

*NumVertices* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex dans le maillage d’origine.

</dd> <dt>

*NumCs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clusters (paramètre d’entrée à compresser).

</dd> <dt>

*pSClusterIDs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Tableau de taille *NumCs* qui contiendra les ID de Super cluster.

</dd> <dt>

*NumSCs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de Super clusters alloués dans [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*pInputIB* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Tampon d’index brut pour le maillage. Le format dépend de *InputIBIs32Bit*.

</dd> <dt>

*InputIBIs32Bit* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, la mémoire tampon d’index est définie sur 32 bits ; dans le cas contraire, 16 bits.

</dd> <dt>

*NumFaces* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de faces dans le maillage d’origine (*pInputIB* est 3 fois cette longueur.)

</dd> <dt>

*ppIBData* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon d’index brute qui contiendra les visages de fractionnement résultants. Format déterminé par *InputIBIs32Bit*. Alloué par la fonction.

</dd> <dt>

*pIBDataLength* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Longueur de *ppIBData*, assignée dans la fonction.

</dd> <dt>

*OutputIBIs32Bit* \[ in, out\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, alloue un tableau d’entiers non signés ; Sinon, alloue un tableau de type short non signé.

</dd> <dt>

*ppFaceRemap* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mappage de chaque visage dans *ppIBData* aux visages d’origine. La longueur est \* *pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Nouvelle structure de données de vertex. Taille de *pVertDataLength*.

</dd> <dt>

*pVertDataLength* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Nombre de nouveaux vertex dans le maillage fractionné. Assigné dans la fonction.

</dd> <dt>

*pSCClusterList* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Tableau de longueur *NumCs* dans lequel *pSCData* indexe ( \* champs pClusterIDs) pour chaque supercluster, contient des clusters triés par supercluster.

</dd> <dt>

*pSCData* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Structure par Super cluster. Contient des index dans *ppIBData*, *pSCClusterList* et *ppVertData*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
