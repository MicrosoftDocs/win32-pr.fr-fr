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
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942181"
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

 

 





