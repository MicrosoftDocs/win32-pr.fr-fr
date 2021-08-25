---
description: Récupère la taille des données binaires. Action déconseillée.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'IDirectXFileBinary :: deDXFile, méthode (. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af59f6a32d163275df02d1469ba4777bf5c5152535c2df52fcf7d7c40218e2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846939"
---
# <a name="idirectxfilebinarygetsize-method"></a>IDirectXFileBinary :: deméthode, méthode

Récupère la taille des données binaires. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PCB* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers la taille retournée des données binaires, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
