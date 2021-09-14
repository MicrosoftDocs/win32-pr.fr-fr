---
title: Commande MCI_CUE (mmsystem. h)
description: La \_ commande MCI CUE signale un appareil afin que la lecture ou l’enregistrement commence par un délai minimal. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- commande MCI_CUE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195155"
---
# <a name="mci_cue-command"></a>\_Commande MCI CUE

La \_ commande MCI CUE signale un appareil afin que la lecture ou l’enregistrement commence par un délai minimal. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_entrée de \_ signal MCI DGV \_
</dt> <dd>

Une instance de vidéo numérique doit préparer l’enregistrement. Si l’application n’a pas d’espace disque réservé, l’appareil réserve l’espace disque à l’aide de ses paramètres par défaut. L’application peut omettre cet indicateur si la source de présentation actuelle est déjà l’entrée externe. (Cet indicateur n’a aucun effet sur la sélection de la source de présentation.)

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV \_ CUE \_ NoShow
</dt> <dd>

Une instance de vidéo numérique doit préparer la diffusion du frame spécifié avec la commande sans l’afficher. Lorsque cet indicateur est spécifié, l’affichage continue d’afficher l’image dans la mémoire tampon de trame, même si son frame correspondant n’est pas la position actuelle. Par exemple, si la mémoire tampon de trame contient l’image du frame 7, l’appareil continue à afficher le cadre 7 lorsque cet indicateur est utilisé pour signaler l’appareil à une autre position. Une commande de pile ultérieure sans cet indicateur et sans l' \_ indicateur MCI pour affiche le frame actuel.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>sortie de la \_ pile MCI DGV \_ \_
</dt> <dd>

Une instance de vidéo numérique doit se préparer à être lue. Si l’espace de travail est suspendu, aucun positionnement ne se produit. Si l’espace de travail est arrêté, la position peut passer à une image d’image clé précédente. L’application peut omettre cet indicateur si la source de présentation actuelle est déjà l’espace de travail.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

La position d’un espace de travail est incluse dans le membre **dwTo** de la structure identifiée par *lpCue*. Les unités affectées aux valeurs de position sont spécifiées à l’aide \_ \_ de l' \_ indicateur de format de temps Set MCI de la commande [ \_ Set MCI](mci-set.md) . Cela équivaut à la recherche d’une position, sauf que l’appareil est suspendu après la commande.

</dd> </dl>

Pour les appareils **Digitalvideo** , le paramètre *lpCue* pointe vers une structure [**MCI \_ DGV \_ CUE \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ à partir de
</dt> <dd>

Le membre **dwFrom** de la structure vers laquelle pointe *lpCue* contient l’emplacement de départ spécifié dans le format d’heure actuel.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Le membre **dwTo** de la structure vers laquelle pointe *lpCue* contient l’emplacement de fin (suspension) spécifié dans le format d’heure actuel.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_entrée de \_ signal de magnétoscope MCI \_
</dt> <dd>

Préparez l’enregistrement.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_sortie de magnétoscope MCI \_ \_
</dt> <dd>

Préparez-vous à la diffusion. Si aucune \_ \_ entrée de la file d’attente MCI magnétoscope et aucune \_ \_ \_ sortie de magnétoscope MCI \_ n’est spécifiée, la sortie de la \_ file d’attente MCI \_ \_ est supposée.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>préroll de \_ magnétoscope MCI \_ \_
</dt> <dd>

Signalez l’appareil à la position actuelle ou à la position **dwFrom** , moins la durée du préroll. Cela permettra à l’appareil de se préparer lui-même avant d’entrer en mode enregistrement ou lecture.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>\_magnétoscope de \_ signal MCI \_ inversé
</dt> <dd>

La direction de la commande de lecture ou d’enregistrement suivante est inversée.

</dd> </dl>

Quand vous cueing pour la lecture à l’aide de la \_ commande MCI CUE avec l' \_ indicateur de sortie MCI VCR \_ \_ , vous pouvez annuler \_ la pile MCI en émettant la commande MCI [ \_ Play](mci-play.md) avec MCI à \_ partir de, MCI \_ à ou \_ magnétoscope MCI \_ Play \_ .

Quand vous cueing à l’enregistrement à l’aide de l' \_ indicateur MCI avec l' \_ \_ indicateur d’entrée de la file d’attente MCI \_ , vous pouvez annuler \_ la pile MCI en émettant la commande d' [ \_ enregistrement MCI](mci-record.md) avec MCI \_ de, MCI \_ à ou \_ \_ l’enregistrement magnétoscope MCI \_ .

Pour les périphériques **VCR** , le paramètre *lpCue* pointe vers une structure de [**file d' \_ \_ attente \_ de magnétoscope MCI**](mci-vcr-cue-parms.md) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_
</dt> <dd>

Un appareil d’entrée Waveform-Audio doit être en signal.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_
</dt> <dd>

Un périphérique de sortie Waveform-Audio doit être en signal. Il s’agit de l’indicateur par défaut si aucun indicateur n’est spécifié.

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

 

