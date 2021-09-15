---
description: Crée une mémoire tampon luminance de transfert précalculée (PRT) compressée à partir d’un objet ID3DXPRTBuffer non compressé. Cette fonction doit être utilisée avec des tampons par vertex ou de volume.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: D3DXCreatePRTCompBuffer, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526084"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>D3DXCreatePRTCompBuffer fonction)

Crée une mémoire tampon luminance de transfert précalculée (PRT) compressée à partir d’un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compressé. Cette fonction doit être utilisée avec des tampons par vertex ou de volume.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Qualité* \[ dans\]
</dt> <dd>

Type : **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Qualité de la compression de l’harmonique sphérique (SH). Consultez [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*NumClusters* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clusters à utiliser pour la compression.

</dd> <dt>

*NumPCA* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vecteurs de base de l’analyse des composants principaux (PCA) à utiliser dans chaque cluster.

</dd> <dt>

*PCB* \[ dans\]
</dt> <dd>

Type : **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Pointeur facultatif vers la fonction de rappel [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) utilisée pour calculer le pourcentage de calculs de compression PRT terminés. La fonction de rappel doit être implémentée pour retourner \_ la valeur OK afin de continuer l’exécution de la routine de compression. Toute autre valeur arrêtera la compression. Peut avoir la **valeur null**.

</dd> <dt>

*lpUserContext* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur facultatif vers une valeur définie par l’utilisateur passée à la fonction de rappel [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) . Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel. Peut avoir la **valeur null**.

</dd> <dt>

*pbuffer* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compressé qui sera compressé.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Adresse d’un pointeur vers l’objet [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
