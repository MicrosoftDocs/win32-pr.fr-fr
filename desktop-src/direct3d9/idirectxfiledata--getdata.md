---
description: Récupère les données de l’un des membres de l’objet ou les données de tous les membres. Action déconseillée.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'IDirectXFileData :: GetData, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 428bff1f3fd76cd7c4589d5084435f8a675ab0d73bf0ff02052b2212d2c2dea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728965"
---
# <a name="idirectxfiledatagetdata-method"></a>IDirectXFileData :: GetData, méthode

Récupère les données de l’un des membres de l’objet ou les données de tous les membres. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szMember* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom du membre pour lequel récupérer des données. Spécifiez **null** pour récupérer tous les données des membres requis.

</dd> <dt>

*PCB* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur qui reçoit la taille de la mémoire tampon ppvData, en octets.

</dd> <dt>

*ppvData* \[ à\]
</dt> <dd>

Type : **void \* \***

Adresse d’un pointeur vers la mémoire tampon pour recevoir les données associées à szMember. Si szMember a la **valeur null**, ppvData est défini pour pointer vers une mémoire tampon contenant toutes les données des membres requis dans un bloc de mémoire contigu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Remarques

Cette méthode récupère les données pour les membres requis d’un objet de données, mais aucune donnée pour les membres facultatifs (enfants). Utilisez [**IDirectXFileData :: GetNextObject**](idirectxfiledata--getnextobject.md) pour récupérer des objets enfants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
