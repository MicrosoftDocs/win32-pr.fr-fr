---
description: Récupère un pointeur vers le nom d’un objet de fichier DirectX. Action déconseillée.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'IDirectXFileObject :: GetName, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e67381a26e3d0f1031e282d6530562416919e8cf52800a07301bf18820887828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846949"
---
# <a name="idirectxfileobjectgetname-method"></a>IDirectXFileObject :: GetName, méthode

Récupère un pointeur vers le nom d’un objet de fichier DirectX. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pstrNameBuf* \[ à\]
</dt> <dd>

Type : **[ **LPSTR**](../winprog/windows-data-types.md)**

Pointeur vers la mémoire tampon dans laquelle le nom de l’objet fichier DirectX sera copié. Affectez la valeur **null** si seule la longueur de la mémoire tampon est nécessaire.

</dd> <dt>

*pdwBufLen* \[ in, out\]
</dt> <dd>

Type : **[ **LPDWORD**](../winprog/windows-data-types.md)**

Pointeur vers une valeur DWORD spécifiant la longueur de la mémoire tampon vers laquelle pointe pstrNameBuf. La valeur du paramètre pdwBufLen sera modifiée en fonction de la longueur de la mémoire tampon nécessaire pour contenir le nom de l’objet, même si pstrNameBuf est **null**. Dans les deux cas, la fonction retourne DXFILEERR \_ BADVALUE si la valeur d’origine de pdwBufLen n’est pas aussi grande que la longueur nécessaire pour contenir le nom de l’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 
