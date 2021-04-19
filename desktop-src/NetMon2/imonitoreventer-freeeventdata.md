---
description: La méthode FreeEventData libère de l’espace alloué pour la structure NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'IMonitorEventer :: FreeEventData, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517229"
---
# <a name="imonitoreventerfreeeventdata-method"></a>IMonitorEventer :: FreeEventData, méthode

La méthode **FreeEventData** libère de l’espace alloué pour la structure [**NMEVENTDATA**](nmeventdata.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNMEventData* \[ dans\]
</dt> <dd>

Adresse de la structure [**NMEVENTDATA**](nmeventdata.md) , dont la mémoire est libérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne S \_ OK.

## <a name="remarks"></a>Notes

Les analyses appellent cette méthode pour libérer la mémoire qu’elles allouent pour la structure des données d’événement. Sachez que bien que le moniteur ait toujours un pointeur vers des chaînes dans une structure [**NMEVENTDATA**](nmeventdata.md) allouée, la mémoire de ces chaînes doit être libérée avant l’appel de la méthode **FreeEventData** .

Pour plus d’informations sur la façon d’allouer de la mémoire pour une structure [**NMEVENTDATA**](nmeventdata.md) , consultez [**IMonitorEventer :: GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




