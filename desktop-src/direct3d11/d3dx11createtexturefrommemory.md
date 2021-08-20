---
title: D3DX11CreateTextureFromMemory, fonction (D3DX11. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser ces bibliothèques DirectXTK (Runtime), CreateXXXTextureFromMemory (où XXX est DDS ou WIC) DirectXTex Library (outils), LoadFromXXXMemory (où XXX est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA en tant que format de source d’art courant pour les jeux), puis CreateTexture créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.'
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- Fonction D3DX11CreateTextureFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17ed4fb842d3a14ed1f8bde2e9371c134e98ba61a54cbde32c98b7fe3939bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099585"
---
# <a name="d3dx11createtexturefrommemory-function"></a>D3DX11CreateTextureFromMemory fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :
>
> -   Bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (où xxx est DDS ou WIC)
> -   Bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis **CreateTexture**

 

Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Pointeur vers l’appareil (consultez [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui utilisera la ressource.

</dd> <dt>

*pSrcData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers la ressource dans la mémoire système.

</dd> <dt>

*SrcDataSize* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**

Taille de la ressource dans la mémoire système.

</dd> <dt>

*pLoadInfo* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***

Facultatif. Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.

</dd> <dt>

*pPump* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)). Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.

</dd> <dt>

*ppTexture* \[ à\]
</dt> <dd>

Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***

Adresse d’un pointeur vers la ressource créée. Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*pHResult* \[ à\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**. Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

