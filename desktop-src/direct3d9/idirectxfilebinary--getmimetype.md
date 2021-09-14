---
description: Récupère le type MIME (Multipurpose Internet Mail Extensions) pour les données binaires. Action déconseillée.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'IDirectXFileBinary :: GetMimeType, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118433"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>IDirectXFileBinary :: GetMimeType, méthode

Récupère le type MIME (Multipurpose Internet Mail Extensions) pour les données binaires. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszMimeType* \[ à\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Adresse d’un pointeur pour recevoir la chaîne de type MIME.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Notes

Quand aucun type MIME n’est spécifié dans un fichier DirectX pour un objet binaire, la fonction affecte à pszMimeType la **valeur null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
