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
ms.openlocfilehash: f2bf462ef63045c8c4e5822e3d28fc21b44dfeed5848da3ac89c8232dfacc062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037439"
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

## <a name="remarks"></a>Remarques

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

 

 




