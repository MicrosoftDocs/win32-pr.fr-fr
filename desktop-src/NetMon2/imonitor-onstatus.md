---
description: La méthode MCSVC appelle la méthode OnStatus pour notifier à l’analyse qu’un événement de statut NPP existe. Cette méthode doit être implémentée par l’analyse.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'IMonitor :: OnStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114146"
---
# <a name="imonitoronstatus-method"></a>IMonitor :: OnStatus, méthode

La méthode MCSVC appelle la méthode **OnStatus** pour notifier à l’analyse qu’un événement de statut NPP existe. Cette méthode doit être implémentée par l’analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Événement* \[ dans\]
</dt> <dd>

Structure [d' \_ événement de mise à jour](update-event.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est \_ OK (ce qui est identique à NOERROR) et MCSVC renvoie la valeur retournée au NPP pour traitement.

Si la méthode échoue, retourne un code d’erreur. En cas d’erreur, MCSVC renvoie la valeur retournée au NPP pour traitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




