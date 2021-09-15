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
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403733"
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

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
