---
description: 'Fonction D3DXGetImageInfoFromResource : récupère des informations sur une image donnée dans une ressource.'
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: D3DXGetImageInfoFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114447"
---
# <a name="d3dxgetimageinfofromresource-function"></a>D3DXGetImageInfoFromResource fonction)

Récupère des informations sur une image donnée dans une ressource.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Module dans lequel la ressource est chargée. Affectez la valeur **null** à ce paramètre pour spécifier le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.

</dd> <dt>

*pSrcFile* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*pSrcInfo* \[ dans\]
</dt> <dd>

Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec la description des données dans le fichier source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes 

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXGetImageInfoFromResourceW. Dans le cas contraire, l’appel de fonction est résolu en D3DXGetImageInfoFromResourceA, car les chaînes ANSI sont utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFile**](d3dxgetimageinfofromfile.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
