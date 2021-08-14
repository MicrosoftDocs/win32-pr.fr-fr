---
title: Commande MCI_RECORD (mmsystem. h)
description: La \_ commande d’enregistrement MCI démarre l’enregistrement à partir de la position actuelle ou d’un emplacement spécifié vers un autre emplacement spécifié.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- commande MCI_RECORD Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327b9ed9b138b581bec17d8bfcfe19ae67bb07d59be2781af54e22a85e2133c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803450"
---
# <a name="mci_record-command"></a>\_Commande d’enregistrement MCI

La commande d' [**\_ enregistrement MCI**](mci-record-parms.md) démarre l’enregistrement à partir de la position actuelle ou d’un emplacement spécifié vers un autre emplacement spécifié. Les périphériques VCR et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
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

MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ . Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ enregistrement MCI**](mci-record-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Cette commande est prise en charge par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur d’enregistrement MCI GETDEVCAPS \_ CAN \_ . Pour le pilote MCIWAVE, toutes les données enregistrées après l’ouverture d’un fichier sont ignorées si le fichier est fermé sans l’enregistrer.

Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge l' \_ enregistrement MCI :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpRecord*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) . Si MCI \_ à partir de n’est pas spécifié, l’emplacement de départ prend par défaut la position actuelle.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_insertion d’enregistrement MCI \_
</dt> <dd>

Les informations nouvellement enregistrées doivent être insérées ou collées dans les données existantes. Il se peut que certains appareils ne prennent pas en charge cette opération. S’il est pris en charge, il s’agit de la valeur par défaut.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_remplacement d’enregistrement MCI \_
</dt> <dd>

Les données doivent remplacer les données existantes. MCIWAVE. L’appareil DRV retourne une \_ fonction non prise en charge MCIERR \_ en réponse à cet indicateur.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpRecord*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) . Si MCI \_ à n’est pas spécifié, l’emplacement de fin se trouve par défaut à la fin du contenu.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI \_ DGV \_ enregistrement \_ audio \_ Stream
</dt> <dd>

Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpRecord*. Si vous omettez cet indicateur, les données audio sont enregistrées dans le premier flux physique.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_blocage d' \_ enregistrement \_ DGV MCI
</dt> <dd>

Lorsque l’enregistrement s’arrête, l’écran contiendra la dernière image et ne reprend pas l’affichage de la vidéo tant qu’une commande [MCI \_ Monitor](mci-monitor.md) n’est pas émise.

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_ \_ \_ flux vidéo de l’enregistrement DGV MCI \_
</dt> <dd>

Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpRecord*. Si vous omettez cet indicateur, les données vidéo sont enregistrées dans le premier flux physique.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_
</dt> <dd>

Un rectangle est spécifié dans le membre **RC** de la structure identifiée par *lpRecord*. Le rectangle spécifie la région de l’entrée externe utilisée comme source pour les pixels compressés et enregistrés. Par défaut, ce rectangle est le rectangle spécifié (ou par défaut) par l' \_ indicateur MCI DGV \_ put \_ Video pour la commande [ \_ put MCI](mci-put.md) . Lorsqu’il est défini différemment du rectangle vidéo, ce qui est affiché n’est pas ce qui est enregistré

</dd> </dl>

Pour les périphériques vidéo numériques, *lpRecord* pointe vers une structure de gestion des [**\_ \_ enregistrements \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_enregistrement magnétoscope \_ MCI \_ à l’adresse
</dt> <dd>

Le membre **dwAt** de la structure identifiée par *lpRecord* contient une heure à laquelle l’intégralité de la commande commence ou, si l’appareil est reçu, lorsque l’appareil atteint la position à partir de la commande CUE.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_initialisation de \_ l’enregistrement magnétoscope \_ MCI
</dt> <dd>

Recherchez l’appareil au début du support, commencez l’enregistrement de la vidéo et de l’audio vides, puis enregistrez le code temporel, si possible.

</dd> </dl>

Pour les périphériques VCR, *lpRecord* pointe vers une structure d' [**\_ \_ enregistrement \_ de magnétoscope MCI**](mci-vcr-record-parms.md) .

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

 

