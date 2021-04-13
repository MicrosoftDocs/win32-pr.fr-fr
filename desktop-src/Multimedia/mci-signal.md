---
title: Commande MCI_SIGNAL (mmsystem. h)
description: La \_ commande de signal MCI définit une position spécifiée dans l’espace de travail. Les périphériques vidéo numériques reconnaissent cette commande. MCIAVI ne prend en charge qu’un seul signal actif à la fois.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Commande MCI_SIGNAL Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384476"
---
# <a name="mci_signal-command"></a>\_Commande de signal MCI

La \_ commande de signal MCI définit une position spécifiée dans l’espace de travail. Les périphériques vidéo numériques reconnaissent cette commande. MCIAVI ne prend en charge qu’un seul signal actif à la fois.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Pointeur vers une structure de valeur de [**\_ \_ signal \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

La fenêtre dont vous spécifiez le descripteur dans le membre **dwCallback** de la structure de [**\_ \_ signal \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) reçoit le \_ message mm MCISIGNAL.

Les indicateurs suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_signal MCI DGV \_ à l' \_ adresse
</dt> <dd>

Une position de signal est incluse dans le membre **dwPosition** de la structure identifiée par *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>\_annulation du \_ signal MCI DGV \_
</dt> <dd>

Supprime la position de signal spécifiée par la valeur associée à MCI \_ DGV \_ signal \_ USERVAL.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_signal DGV \_ MCI \_ chaque
</dt> <dd>

Une valeur signal-period est incluse dans le membre **dwPeriod** de la structure identifiée par *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_position du \_ signal MCI DGV \_
</dt> <dd>

L’appareil enverra la valeur de position avec le message Windows au lieu de la valeur spécifiée par l’utilisateur.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV \_ signal \_ USERVAL
</dt> <dd>

Une valeur de données est incluse dans le membre **dwUserParm** de la structure identifiée par *lpSignal*. La valeur de données associée à cette demande est reportée avec le message Windows.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 

