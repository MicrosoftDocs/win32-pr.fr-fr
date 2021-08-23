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
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779039"
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



 

 




