---
title: Commande MCI_COPY (mmsystem. h)
description: La \_ commande de copie MCI copie les données dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- commande MCI_COPY Windows multimédia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590acf61b352fa9abab00dfd49f3f54b166bfc340eaf12061e3d90b7a3025d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039289"
---
# <a name="mci_copy-command"></a>\_Commande de copie MCI

La \_ commande de copie MCI copie les données dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Pointeur vers une structure de [**\_ DGV de \_ copie \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_ \_ copie de DGV MCI à l' \_ adresse
</dt> <dd>

Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpCopy*. Le rectangle spécifie la partie de chaque cadre à copier. Si l’indicateur est omis, la \_ copie MCI copie l’intégralité du frame.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ copier \_ un \_ flux audio
</dt> <dd>

Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpCopy*. Si vous utilisez cet indicateur et que vous souhaitez également copier la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV copier le \_ \_ flux vidéo. (Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont copiées.)

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_ \_ flux vidéo de copie MCI DGV \_ \_
</dt> <dd>

Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpCopy*. Si vous utilisez cet indicateur et que vous souhaitez également copier l’audio, vous devez également utiliser \_ l' \_ indicateur MCI DGV copier le \_ \_ flux audio. (Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont copiées.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpCopy*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpCopy*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la \_ commande Set MCI.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



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

 

