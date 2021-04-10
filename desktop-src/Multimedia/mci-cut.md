---
title: Commande MCI_CUT (mmsystem. h)
description: La \_ commande MCI Cut supprime les données du fichier et les copie dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Commande MCI_CUT Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942438"
---
# <a name="mci_cut-command"></a>\_Commande MCI Cut

La \_ commande MCI Cut supprime les données du fichier et les copie dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
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

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*
</dt> <dd>

Pointeur vers une structure [**MCI \_ DGV \_ Cut \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_DGV MCI \_ \_ à
</dt> <dd>

Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpCut*. Le rectangle spécifie la partie de chaque cadre à couper. Si l’indicateur est omis, MCI \_ coupe le cadre entier.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI \_ DGV \_ couper \_ le \_ flux audio
</dt> <dd>

Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpCut*. Si vous utilisez cet indicateur et que vous souhaitez également couper la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV Cut \_ Video \_ Stream. (Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont coupées.)

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_ \_ flux vidéo de coupure MCI DGV \_ \_
</dt> <dd>

Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpCut*. Si vous utilisez cet indicateur et que vous souhaitez également couper le son, vous devez également utiliser \_ l' \_ indicateur MCI DGV couper le \_ \_ flux audio. (Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont coupées.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpCut*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpCut*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.

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

 

