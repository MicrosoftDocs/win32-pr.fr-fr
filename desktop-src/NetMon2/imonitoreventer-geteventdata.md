---
description: La méthode GetEventData alloue de l’espace pour les structures NMEVENTDATA et NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'IMonitorEventer :: GetEventData, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3a089e57ac5f66187f97dfa6ae7533aeda620632bdbf35c7b5bf3a34d4654b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037369"
---
# <a name="imonitoreventergeteventdata-method"></a>IMonitorEventer :: GetEventData, méthode

La méthode **GetEventData** alloue de l’espace pour les structures [NMEVENTDATA](nmeventdata.md) et [NMCOLUMNINFO](nmcolumninfo.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bNumColumns* \[ dans\]
</dt> <dd>

Nombre de structures **NMCOLUMNINFO** nécessaires.

</dd> <dt>

*ppNMEventData* \[ à\]
</dt> <dd>

Adresse de la structure **NMEVENTDATA** retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est S \_ OK.

Si la méthode échoue, la valeur de retour est NMERR à une \_ mémoire insuffisante \_ \_ .

## <a name="remarks"></a>Remarques

Les analyses appellent cette méthode pour allouer de la mémoire aux structures d’informations de colonne et de données d’événement. Pour libérer la mémoire allouée pour une structure **NMEVENTDATA** , consultez [IMonitorEventer :: FreeEventData](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IMonitorEventer](imonitoreventer.md)
</dt> <dt>

[IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md)
</dt> <dt>

[NMEVENTDATA](nmeventdata.md)
</dt> <dt>

[NMCOLUMNINFO](nmcolumninfo.md)
</dt> </dl>

 

 




