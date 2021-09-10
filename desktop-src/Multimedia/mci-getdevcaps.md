---
title: Commande MCI_GETDEVCAPS (mmsystem. h)
description: La \_ commande MCI GETDEVCAPS récupère des informations statiques sur un appareil.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- commande MCI_GETDEVCAPS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363763"
---
# <a name="mci_getdevcaps-command"></a>\_Commande MCI GETDEVCAPS

La \_ commande MCI GETDEVCAPS récupère des informations statiques sur un appareil. Tous les appareils reconnaissent cette commande. Les paramètres et indicateurs disponibles pour cette commande dépendent de l’appareil sélectionné. Les informations sont retournées dans le membre **dwReturn** de la structure identifiée par *lpCapsParms*.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
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

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Pointeur vers une structure [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs standard et spécifiques à la commande suivants s’appliquent à tous les appareils prenant en charge MCI \_ GETDEVCAPS :

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ périphérique composite MCI GETDEVCAPS \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil utilise le stockage de données qui doit être ouvert et fermé explicitement ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_type d' \_ appareil \_ GETDEVCAPS MCI
</dt> <dd>

Le membre **dwReturn** est défini sur l’une des valeurs indiquées dans [types d’appareils MCI](mci-device-types.md).

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ a un \_ son
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil a une sortie audio ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ a une \_ vidéo
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil a une sortie vidéo ; elle a la valeur **false** dans le cas contraire. Par exemple, le membre a la valeur **true** pour les appareils qui prennent en charge le jeu de commandes videodisc.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_élément GETDEVCAPS \_ MCI
</dt> <dd>

Spécifie que le membre **dwItem** de la structure [**\_ \_ GETDEVCAPSs MCI**](mci-getdevcaps-parms.md) contient l’une des constantes suivantes :

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ peut \_ éjecter
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut éjecter le média ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ peut \_ jouer
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut lire le média. dans le cas contraire, il est défini sur **false**. Si un appareil spécifie la **valeur true**, cela signifie que l’appareil prend en charge les commandes [MCI \_ Pause](mci-pause.md) et [ \_ Stop MCI](mci-stop.md) , ainsi que la commande de [ \_ lecture MCI](mci-play.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ peut \_ Enregistrer
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil prend en charge l’enregistrement ; dans le cas contraire, il est défini sur **false**. Si un appareil spécifie la **valeur true**, cela signifie que l’appareil prend en charge les \_ commandes de pause MCI et d’arrêt MCI, ainsi \_ que la commande d' [ \_ enregistrement MCI](mci-record.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ peut \_ Enregistrer
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut enregistrer un fichier ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ utilise des \_ fichiers
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil requiert un nom de fichier ; elle a la valeur **false** dans le cas contraire. Seuls les appareils composés utilisent des fichiers.

</dd> </dl>

Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ peut se \_ figer
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut geler des frames ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ peut être \_ verrouillé
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut se verrouiller ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>la \_ GETDEVCAPS DGV MCI \_ \_ peut être \_ inversée
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut jouer en sens inverse ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ peut être \_ Str \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut étirer l’entrée ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>\_DGV \_ GETDEVCAPS MCI \_ peut être \_ étiré
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut étirer une image ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>\_test de \_ GETDEVCAPS \_ DGV \_ MCI
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut effectuer des tests ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ a \_ toujours
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut afficher des images fixes ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ Max \_ Windows
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre maximal de fenêtres que l’appareil peut gérer simultanément.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>débit maximal de MCI \_ DGV \_ GETDEVCAPS \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la vitesse de lecture maximale pour l’appareil, en images par seconde.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>taux minimal de MCI \_ DGV \_ GETDEVCAPS \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la vitesse de lecture minimale de l’appareil, en images par seconde.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ palettes MCI DGV GETDEVCAPS \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut retourner un handle de palette ; dans le cas contraire, il est défini sur **false**.

</dd> </dl>

Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>taux d’incrément de l' \_ horloge MCI GETDEVCAPS \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre d’incréments par seconde.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut \_ détecter une \_ longueur
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de détecter la longueur du média. dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut se \_ figer
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de figer l’image de sortie ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut \_ surveiller les \_ sources
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de surveiller les sources ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ peut être \_ préroll
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité d’effectuer un préroll ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut \_ prévisualiser
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité d’afficher des préversions ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ peut être \_ inversé
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de fonctionner en sens inverse. dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ peut être \_ testé
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de tester ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ magnétoscope \_ GETDEVCAPS \_ avec \_ horloge
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil prend en charge une horloge externe. dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ a un \_ code temporel
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil dispose d’une fonctionnalité de code temporel ou si cette fonctionnalité est inconnue. dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_magnétoscope MCI \_ GETDEVCAPS \_ nombre \_ de \_ marques
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre de marques (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>précision de la \_ recherche MCI VCR \_ GETDEVCAPS \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la précision de la recherche de l’appareil.

</dd> </dl>

Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ peut se \_ figer
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut geler l’image ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>\_OVLY \_ GETDEVCAPS MCI \_ peut être \_ étiré
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil peut étirer l’image pour remplir le frame ; dans le cas contraire, il est défini sur **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ Max \_ Windows
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre maximal de fenêtres que l’appareil peut gérer simultanément.

</dd> </dl>

Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil **videodisc** :

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ peut \_ inverser
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le lecteur videodisc peut jouer en sens inverse ; dans le cas contraire, il est défini sur **false**. Certains lecteurs peuvent lire des disques CLV à l’inverse, ainsi que des disques CAV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ \_ GETDEVCAPS \_ CAV
</dt> <dd>

En cas de combinaison avec d’autres éléments, spécifie que les informations de retour s’appliquent au format CAV videodiscs. Il s’agit de la valeur par défaut si aucun videodisc n’est inséré.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ \_ GETDEVCAPS \_ CLV
</dt> <dd>

En cas de combinaison avec d’autres éléments, spécifie que les informations de retour s’appliquent au format CLV videodiscs.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_taux de FAST MCI VD \_ GETDEVCAPS \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le taux de lecture rapide standard en images par seconde.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>taux normal de MCI \_ VD \_ GETDEVCAPS \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la vitesse de lecture normale en images par seconde.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>\_ \_ taux lent de GETDEVCAPS MCI VD \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le taux de lecture lent standard en images par seconde.

</dd> </dl>

Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_entrée MCI Wave \_ GETDEVCAPS \_
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre total d’appareils d’entrée (enregistrement) de la forme d’onde.

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_sortie MCI Wave \_ GETDEVCAPS \_
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre total d’appareils de sortie de forme d’onde (lecture).

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

 

