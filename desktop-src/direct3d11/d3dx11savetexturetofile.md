---
title: D3DX11SaveTextureToFile, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, CaptureTexture Then SaveToXXXFile (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Pour le scénario simplifié de création d’une capture d’écran à partir d’une texture de cible de rendu, nous vous recommandons d’utiliser la bibliothèque DirectXTK, SaveDDSTextureToFile ou SaveWICTextureToFile. Enregistrer une texture dans un fichier.'
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Fonction D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974587"
---
# <a name="d3dx11savetexturetofile-function"></a>D3DX11SaveTextureToFile fonction)

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** Then **SAVETOXXXFILE** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Pour le scénario simplifié de création d’une capture d’écran à partir d’une texture de cible de rendu, nous vous recommandons d’utiliser la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** ou **SaveWICTextureToFile**.

 

Enregistrer une texture dans un fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* 
</dt> <dd>

Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pSrcTexture* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Pointeur vers la texture à enregistrer. Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ dans\]
</dt> <dd>

Type : **[ **D3DX11 \_ image \_ file \_ format**](d3dx11-image-file-format.md)**

Format dans lequel la texture sera enregistrée (voir [**format de \_ \_ fichier image \_ D3DX11**](d3dx11-image-file-format.md)). D3DX11 \_ IFF \_ DDS est le format par défaut, car il s’agit de la seule option qui prend en charge tous les formats au [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom du fichier de sortie de destination dans lequel la texture sera enregistrée. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs énumérées dans les [codes de retour de Direct3D 11](d3d11-graphics-reference-returnvalues.md). Utilisez la valeur de retour pour voir si le *DestFormat* est pris en charge.

## <a name="remarks"></a>Notes

**D3DX11SaveTextureToFile** écrit la structure [**\_ \_ DXT10 en-tête DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) supplémentaire pour la texture d’entrée uniquement si nécessaire (par exemple, parce que la texture d’entrée est au format RVB standard (sRVB)). Si **D3DX11SaveTextureToFile** écrit la structure **DXT10 de l' \_ en-tête \_ DDS** , il définit le membre **dwFourCC** de la structure [**DDS \_ PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) pour la texture sur **facilement** pour indiquer le Prescense de l’en-tête étendu DXT10 de l' **\_ en-tête \_ DDS** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

