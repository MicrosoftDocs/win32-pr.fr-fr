---
description: Récupère des informations sur une image donnée dans une ressource.
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: D3DX10GetImageInfoFromResource, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e77efb973e20a5db708d28b49f0cee27bee7d4e5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211715"
---
# <a name="d3dx10getimageinfofromresource-function"></a>D3DX10GetImageInfoFromResource fonction)

Récupère des informations sur une image donnée dans une ressource.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Module dans lequel la ressource est chargée. Affectez la valeur **null** à ce paramètre pour spécifier le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*pPump* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone. Peut avoir la **valeur null**. Consultez [**ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> <dt>

*pSrcInfo* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ informations sur l’image d3dx10**](d3dx10-image-info.md)\***

Pointeur vers une \_ structure d’informations d’image d3dx10 \_ à remplir avec la description des données dans le fichier source.

</dd> <dt>

*pHResult* \[ à\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**. Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DX10GetImageInfoFromResourceW. Dans le cas contraire, l’appel de fonction est résolu en D3DX10GetImageInfoFromResourceA, car les chaînes ANSI sont utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de texture dans D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
