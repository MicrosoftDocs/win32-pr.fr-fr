---
description: Enregistrer une texture dans un fichier.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: D3DX10SaveTextureToFile, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d1adb4a490b047329277c4092a68563ffc4bf5d4bb1dbfd866bb849d9f561a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634559"
---
# <a name="d3dx10savetexturetofile-function"></a>D3DX10SaveTextureToFile fonction)

Enregistrer une texture dans un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
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

Format dans lequel la texture sera enregistrée (voir [**format de \_ \_ fichier image \_ d3dx10**](d3dx10-image-file-format.md)). D3DX10 \_ IFF \_ DDS est le format par défaut, car il s’agit de la seule option qui prend en charge tous les formats au [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nom du fichier de sortie de destination dans lequel la texture sera enregistrée. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md). Utilisez la valeur de retour pour voir si le *DestFormat* est pris en charge.

## <a name="remarks"></a>Remarques

**D3DX10SaveTextureToFile** écrit la structure [**\_ \_ DXT10 en-tête DDS**](../direct3ddds/dds-header-dxt10.md) supplémentaire pour la texture d’entrée uniquement si nécessaire (par exemple, parce que la texture d’entrée est au format RVB standard (sRVB)). Si **D3DX10SaveTextureToFile** écrit la structure **DXT10 de l' \_ en-tête \_ DDS** , il définit le membre **dwFourCC** de la structure [**DDS \_ PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) pour la texture sur **facilement** pour indiquer le Prescense de l’en-tête étendu DXT10 de l' **\_ en-tête \_ DDS** .

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

 

 
