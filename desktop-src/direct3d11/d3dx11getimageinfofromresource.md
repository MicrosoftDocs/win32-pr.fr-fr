---
title: D3DX11GetImageInfoFromResource, fonction (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les fonctions de ressource, puis d’utiliser la bibliothèque DirectXTex (outils), LoadFromXXXMemory (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Récupère des informations sur une image donnée dans une ressource.'
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Fonction D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ada8118dac3e39f9f91012bb3ec681db7b156540cffae0fb7c0f1a7bc1819b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535954"
---
# <a name="d3dx11getimageinfofromresource-function"></a>D3DX11GetImageInfoFromResource fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les [fonctions de ressource](/windows/desktop/menurc/resources-functions), puis d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.

 

Récupère des informations sur une image donnée dans une ressource.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Module dans lequel la ressource est chargée. Affectez la valeur **null** à ce paramètre pour spécifier le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*pPump* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone. Peut avoir la **valeur null**. Voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***

Pointeur vers une \_ structure d’informations d’image D3DX11 \_ à remplir avec la description des données dans le fichier source.

</dd> <dt>

*pHResult* \[ à\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**. Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en **D3DX11GetImageInfoFromResourceW**. Dans le cas contraire, l’appel de fonction est résolu en **D3DX11GetImageInfoFromResourceA** , car les chaînes ANSI sont utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

