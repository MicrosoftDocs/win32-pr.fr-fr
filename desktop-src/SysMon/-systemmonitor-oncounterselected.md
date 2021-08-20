---
title: Événement SystemMonitor. OnCounterSelected
description: Vous avertit lorsqu’un compteur est sélectionné.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Événement OnCounterSelected SysMon
- Événement OnCounterSelected SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, événement OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e5402eb123c5edd44a5616b6973940ba065e2b0c8c2bfa63e7d151ae30124
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957246"
---
# <a name="systemmonitoroncounterselected-event"></a>Événement SystemMonitor. OnCounterSelected

Vous avertit lorsqu’un compteur est sélectionné.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index du compteur sélectionné dans l’objet de collection de [**compteurs**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Vous pouvez recevoir cet événement lorsque

-   Vous définissez [**CounterItem. Selected**](counteritem-selected.md) sur true
-   L’utilisateur sélectionne un compteur dans la légende
-   L’utilisateur double-clique sur un compteur dans la légende

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





