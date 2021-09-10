---
title: Commande MCI_MONITOR (mmsystem. h)
description: La \_ commande MCI Monitor spécifie la source de la présentation. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- commande MCI_MONITOR Windows multimédia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363804"
---
# <a name="mci_monitor-command"></a>\_Commande MCI Monitor

La \_ commande MCI Monitor spécifie la source de la présentation. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificateur de l’appareil MCI qui doit recevoir le message de commande.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, MCI \_ Wait ou MCI \_ test. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*
</dt> <dd>

Pointeur vers une structure [**MCI \_ DGV \_ Monitor \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_méthode d' \_ analyse \_ DGV MCI
</dt> <dd>

Une constante indiquant que la méthode de surveillance est incluse dans le membre **dwMethod** de la structure identifiée par *lpMonitor*.

Lorsque l' \_ \_ indicateur d’entrée du moniteur MCI DGV \_ est utilisé dans le membre **dwSource** , cela sélectionne la méthode de surveillance. En règle générale, les différentes méthodes d’analyse ont des implications différentes sur la façon dont le matériel est utilisé. La méthode d’analyse par défaut est sélectionnée par l’appareil.

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_source du \_ moniteur MCI DGV \_
</dt> <dd>

Une constante indiquant que la source du moniteur est incluse dans le membre **dwSource** de la structure identifiée par *lpMonitor*.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 

