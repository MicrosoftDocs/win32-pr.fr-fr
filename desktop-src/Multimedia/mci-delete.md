---
title: Commande MCI_DELETE (mmsystem. h)
description: La \_ commande MCI Delete supprime les données du fichier. Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- commande MCI_DELETE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195148"
---
# <a name="mci_delete-command"></a>\_Commande de suppression MCI

La \_ commande MCI Delete supprime les données du fichier. Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
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

MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ . Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs suivants s’appliquent au type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ supprimer \_ à
</dt> <dd>

Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpDelete*. Le rectangle spécifie la partie de chaque cadre à supprimer. Lorsque cet indicateur est utilisé, le frame est conservé dans l’espace de travail et la zone spécifiée par le rectangle devient noire. Si l’indicateur est omis, MCI \_ supprime par défaut l’ensemble du frame et supprime le frame de l’espace de travail.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ supprimer \_ le \_ flux audio
</dt> <dd>

Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpDelete*. Si vous utilisez cet indicateur et que vous souhaitez également supprimer la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV supprimer le \_ \_ flux vidéo. (Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont supprimées.)

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_ \_ flux vidéo de suppression de DGV MCI \_ \_
</dt> <dd>

Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpDelete*. Si vous utilisez cet indicateur et que vous souhaitez également supprimer l’audio, vous devez également utiliser \_ l' \_ indicateur MCI DGV supprimer le \_ \_ flux audio. (Si aucun indicateur n’est spécifié, les données de tous les flux audio et vidéo sont supprimées.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpDelete*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpDelete*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpDelete* pointe vers une structure [**MCI \_ DGV \_ Delete \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .

Les indicateurs suivants s’appliquent au type d’appareil **WaveAudio** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpDelete*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' [ \_ ensemble MCI](mci-set.md).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpDelete*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI.

</dd> </dl>

Pour les périphériques audio Waveform, le paramètre *lpDelete* pointe vers une structure [**MCI \_ Wave \_ supprimer \_ PARMS**](mci-wave-delete-parms.md) .

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

 

