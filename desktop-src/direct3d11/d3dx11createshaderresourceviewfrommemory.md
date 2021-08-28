---
title: D3DX11CreateShaderResourceViewFromMemory, fonction (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser ces bibliothèques DirectXTK (Runtime), CreateXXXTextureFromMemory (où XXX est DDS ou WIC) DirectXTex Library (outils), LoadFromXXXMemory (où XXX est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA en tant que format de source d’art courant pour les jeux), puis CreateShaderResourceView créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.'
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- Fonction D3DX11CreateShaderResourceViewFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d242885fc09ee513f5107298f1bac98b5cb9cb684de0f6e85e960fb9c7078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124734"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a>D3DX11CreateShaderResourceViewFromMemory fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :
>
> -   Bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (où xxx est DDS ou WIC)
> -   Bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis **CreateShaderResourceView**

 

Créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
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

Pointeur vers le fichier en mémoire qui contient l’affichage des ressources du nuanceur.

</dd> <dt>

*SrcDataSize* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**

Taille du fichier en mémoire.

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

*ppShaderResourceView* \[ à\]
</dt> <dd>

Type : **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Adresse d’un pointeur vers l’affichage des ressources de nuanceur nouvellement créé. Consultez [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> <dt>

*pHResult* \[ à\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**. Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

