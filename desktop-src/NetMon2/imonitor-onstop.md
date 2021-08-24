---
description: La méthode OnStop doit être implémentée par l’analyse. Le MSCVC appelle cette méthode pour informer le moniteur que la capture sera arrêtée.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'IMonitor :: OnStop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: cb81042395de2a2381921cfd0b30c18af22df320b8ce8db228cf65743b1fe334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778989"
---
# <a name="imonitoronstop-method"></a>IMonitor :: OnStop, méthode

La méthode **OnStop** doit être implémentée par l’analyse. Le MSCVC appelle cette méthode pour informer le moniteur que la capture sera arrêtée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).

Si la méthode échoue, la valeur de retour est un code d’erreur. Lorsqu’un code d’erreur est retourné, l’analyse ne peut pas être redémarrée.

## <a name="remarks"></a>Remarques

MCSVC appelle cette méthode après l’appel de [IRTC :: Stop](irtc-stop.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




