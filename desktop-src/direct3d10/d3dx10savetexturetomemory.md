---
description: Enregistrer une texture dans la mémoire.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: D3DX10SaveTextureToMemory, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531339"
---
# <a name="d3dx10savetexturetomemory-function"></a>D3DX10SaveTextureToMemory fonction)

Enregistrer une texture dans la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrcTexture* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Pointeur vers la texture à enregistrer. Voir [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ dans\]
</dt> <dd>

Type : **[ **d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md)**

Format dans lequel la texture sera enregistrée. Consultez [**\_ format de \_ fichier \_ image d3dx10**](d3dx10-image-file-format.md).

</dd> <dt>

*ppDestBuf* \[ à\]
</dt> <dd>

Type : **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Adresse d’un pointeur vers la mémoire contenant la texture enregistrée. Voir [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Optionnel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
