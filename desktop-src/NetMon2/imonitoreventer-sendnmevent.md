---
description: la méthode SendNMEvent soumet des événements à Windows Management Instrumentation (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'IMonitorEventer :: SendNMEvent, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a922dbbd3e31fc344383016416f139424fd5782e9bf92268e3fb4ff1dc7f93b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037359"
---
# <a name="imonitoreventersendnmevent-method"></a>IMonitorEventer :: SendNMEvent, méthode

la méthode **SendNMEvent** soumet des événements à Windows Management Instrumentation (WMI).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNMEventData* \[ dans\]
</dt> <dd>

Pointeur vers l’événement soumis à WMI.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est S \_ OK.

Si la méthode échoue, la valeur de retour est NMERR à une \_ mémoire insuffisante \_ \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




