---
title: Commande MCI_INFO (mmsystem. h)
description: La \_ commande MCI info récupère les informations de chaîne d’un appareil.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Commande MCI_INFO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105709"
---
# <a name="mci_info-command"></a>\_Commande MCI info

La \_ commande MCI info récupère les informations de chaîne d’un appareil. Tous les appareils reconnaissent cette commande. Les informations sont retournées dans le membre **lpstrReturn** de la structure identifiée par *lpInfo*. Le membre **dwRetSize** spécifie la longueur de la mémoire tampon pour les données retournées.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
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

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Pointeur vers une structure d' [**\_ informations \_ sur MCI**](mci-info-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

L’indicateur de code standard et spécifique à la commande suivant s’applique à tous les périphériques prenant en charge MCI \_ info :

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_produit MCI info \_
</dt> <dd>

Obtient une description du matériel associé à un appareil. Les appareils doivent fournir une description qui identifie le pilote et le matériel utilisés.

</dd> </dl>

Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **cdaudio** :

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>\_identité des \_ médias MCI info \_
</dt> <dd>

Produit un identificateur unique pour le CD audio actuellement chargé dans le lecteur interrogé. Cet indicateur retourne une chaîne de 16 chiffres hexadécimaux.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>MCI \_ info \_ Media \_ UPC
</dt> <dd>

Produit le code UPC (Universal Product Code) encodé sur un CD audio. Le UPC est une chaîne de chiffres. Elle n’est peut-être pas disponible pour tous les CD.

</dd> </dl>

Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_élément d' \_ informations \_ DGV MCI
</dt> <dd>

Une constante indiquant les informations souhaitées est incluse dans le membre **dwItem** de la structure identifiée par *lpInfo*. Les constantes suivantes sont définies pour les périphériques vidéo numériques :

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ info \_ audio \_ ALG
</dt> <dd>

Retourne le nom de l’algorithme de compression audio actuel.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>MCI \_ DGV \_ info \_ audio- \_ qualité
</dt> <dd>

Retourne le nom du descripteur de qualité audio actuel.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>\_informations DGV \_ MCI \_ \_
</dt> <dd>

Retourne le nom de l’algorithme de compression d’image continue actuel.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>la \_ qualité des informations DGV MCI est \_ \_ toujours \_
</dt> <dd>

Retourne le nom du descripteur de qualité d’image continue actuel.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_utilisation des \_ informations \_ DGV MCI
</dt> <dd>

Retourne une chaîne qui décrit les restrictions d’utilisation qui peuvent être imposées par le propriétaire des données visuelles ou sonores dans l’espace de travail.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>\_vidéo d' \_ informations \_ DGV \_ MCI
</dt> <dd>

Retourne le nom de l’algorithme de compression vidéo actuel.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_ \_ qualité vidéo des informations DGV \_ MCI \_
</dt> <dd>

Retourne le nom du descripteur de qualité vidéo actuel.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_version d’informations MCI \_
</dt> <dd>

Retourne le niveau de version du pilote de périphérique et du matériel. Les développeurs de pilotes de périphériques doivent documenter la syntaxe de la chaîne retournée.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_texte d' \_ informations \_ DGV MCI
</dt> <dd>

Obtient le titre de la fenêtre.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_
</dt> <dd>

Obtient le chemin d’accès et le nom de fichier du dernier fichier spécifié avec la commande [MCI \_ Open](mci-open.md) ou [MCI \_ Load](mci-load.md) . Si un fichier n’a pas été spécifié, l’appareil retourne une chaîne terminée par le caractère null. Cet indicateur est pris en charge uniquement par les appareils qui retournent la **valeur true** à l' \_ indicateur MCI GETDEVCAPS \_ utilise \_ les fichiers de la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

</dd> </dl>

Pour les périphériques vidéo numériques, *lpInfo* pointe vers une structure [**MCI \_ DGV \_ info \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .

Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **Sequencer** :

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>\_Copyright des informations MCI \_
</dt> <dd>

Obtient l’avis de copyright du fichier MIDI à partir de l’événement de métadonnées de copyright.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_
</dt> <dd>

Obtient le nom du fichier actif. Cet indicateur est pris en charge uniquement par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur MCI GETDEVCAPS \_ utilise des \_ fichiers.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>nom de l' \_ info MCI \_
</dt> <dd>

Obtient le nom de la séquence à partir de l’événement de méta-nom de séquence/suivi.

</dd> </dl>

L’indicateur supplémentaire suivant s’applique au type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_version d' \_ informations \_ magnétoscope MCI
</dt> <dd>

Définit le membre **lpstrReturn** de la structure d' [**\_ informations \_ sur MCI**](mci-info-parms.md) pour qu’il pointe vers le numéro de version. Définit également le membre **dwRetSize** égal à la longueur de la chaîne vers laquelle pointe.

</dd> </dl>

Les indicateurs supplémentaires suivants s’appliquent au type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_
</dt> <dd>

Obtient le nom du fichier actif. Cet indicateur est pris en charge uniquement par les appareils qui retournent la **valeur true** à l' \_ indicateur MCI GETDEVCAPS \_ utilise \_ les fichiers de la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_texte d' \_ informations \_ OVLY MCI
</dt> <dd>

Obtient la légende de la fenêtre associée à l’appareil de superposition vidéo.

</dd> </dl>

Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **WaveAudio** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_fichier d’informations MCI \_
</dt> <dd>

Obtient le nom du fichier actif. Cet indicateur est pris en charge par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur MCI GETDEVCAPS \_ utilise des \_ fichiers.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_
</dt> <dd>

Obtient le nom de produit de l’entrée actuelle.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_
</dt> <dd>

Obtient le nom de produit de la sortie actuelle et sa valeur est spécifique à l’appareil.

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

 

