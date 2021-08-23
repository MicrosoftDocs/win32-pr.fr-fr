---
title: Événement SystemMonitor. OnCounterDeleted
description: Vous avertit avant qu’un compteur soit supprimé de la collection de compteurs.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Événement OnCounterDeleted SysMon
- Événement OnCounterDeleted SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, événement OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c178cb0b9c19fde0814f15729ffd49a0a0dbea65023bde06673cd843aeb668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884001"
---
# <a name="systemmonitoroncounterdeleted-event"></a>Événement SystemMonitor. OnCounterDeleted

Vous avertit avant qu’un compteur soit supprimé de la collection de [**compteurs**](counters.md) .

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index du compteur à supprimer de l’objet de collection de [**compteurs**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





