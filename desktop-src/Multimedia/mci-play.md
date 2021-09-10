---
title: Commande MCI_PLAY (mmsystem. h)
description: La \_ commande MCI Play signale à l’appareil qu’il doit commencer à transmettre des données de sortie. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- commande MCI_PLAY Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363796"
---
# <a name="mci_play-command"></a>\_Commande MCI Play

La \_ commande MCI Play signale à l’appareil qu’il doit commencer à transmettre des données de sortie. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
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

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ lecture MCI**](mci-play-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge MCI \_ Play :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Un emplacement de départ est inclus dans le membre **dwFrom** de la structure identifiée par *lpPlay*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) . Si MCI \_ à partir de n’est pas spécifié, l’emplacement de départ prend par défaut la position actuelle.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Un emplacement de fin est inclus dans le membre **dwTo** de la structure identifiée par *lpPlay*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de l' \_ ensemble MCI. Si \_ vous ne spécifiez pas l’option MCI à, l’emplacement de fin est défini par défaut à la fin du support.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_ \_ lecture \_ répétée MCI DGV
</dt> <dd>

La lecture doit redémarrer à partir du début lorsque la fin du contenu est atteinte.

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>\_ \_ lecture \_ inversée MCI DGV
</dt> <dd>

La lecture doit être effectuée en sens inverse.

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>\_fenêtre de \_ lecture MCI MCIAVI \_
</dt> <dd>

La lecture doit se produire dans la fenêtre associée à une instance d’appareil (valeur par défaut). (Cet indicateur est spécifique à MCIAVI. DRV.)

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI \_ MCIAVI \_ Play \_ fullscreen
</dt> <dd>

La lecture doit utiliser un affichage plein écran. Utilisez cet indicateur uniquement lors de la diffusion de fichiers compressés ou 8 bits.

</dd> </dl>

Pour les périphériques vidéo numériques, *lpPlay* pointe vers une structure [**MCI \_ DGV \_ Play \_ PARMS**](/previous-versions//dd743396(v=vs.85)) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_magnétoscope MCI \_ lu \_ à
</dt> <dd>

Le membre **dwAt** de la structure identifiée par *lpPlay* contient une heure à laquelle l’intégralité de la commande commence ou, si l’appareil est reçu, lorsque l’appareil atteint la position à partir de la commande [MCI \_ CUE](mci-cue.md) .

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>\_ \_ Lecture inversée des MAGNÉTOSCOPEs MCI \_
</dt> <dd>

La lecture doit être effectuée en sens inverse.

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_analyse de \_ lecture \_ magnétoscope MCI
</dt> <dd>

La lecture doit être aussi rapide que possible tout en conservant la sortie vidéo.

</dd> </dl>

Pour les périphériques VCR, *lpPlay* pointe vers une structure de [**\_ \_ lecture \_ de magnétoscope MCI**](mci-vcr-play-parms.md) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **videodisc** :

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>\_Fast de \_ lecture MCI VD \_
</dt> <dd>

Jouez rapidement.

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>\_ \_ lecture \_ inversée MCI VD
</dt> <dd>

Jouez en sens inverse.

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>\_analyse de \_ lecture MCI VD \_
</dt> <dd>

Analyser rapidement.

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI \_ VD \_ Play \_ lent
</dt> <dd>

Jouez lentement.

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_vitesse de \_ lecture MCI VD \_
</dt> <dd>

La vitesse de lecture est incluse dans le membre **dwSpeed** de la structure identifiée par *lpPlay*.

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

 

