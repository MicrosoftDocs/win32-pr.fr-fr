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
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201370"
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

## <a name="remarks"></a>Notes

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

 

 




