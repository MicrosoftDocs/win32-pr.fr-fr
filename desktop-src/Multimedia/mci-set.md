---
title: Commande MCI_SET (mmsystem. h)
description: La \_ commande Set MCI définit les informations de l’appareil. Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.
ms.assetid: c527f9d6-2119-4274-98b7-dc892e9b70f9
keywords:
- commande MCI_SET Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SET
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f5affb6ce41c5c321b24353ece8f0946dc668194ac59cee95e579178a8b03df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803385"
---
# <a name="mci_set-command"></a>\_Commande Set MCI

> [!NOTE]
> Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.  Dans ce document, il existe des références au mot « esclave ». Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.  Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes. Pour des fins de cohérence, ce document contient ce mot. Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.

La \_ commande Set MCI définit les informations de l’appareil. Les périphériques CD audio, numérique-vidéo, MIDI Sequencer, VCR, videodisc, vidéo-overlay et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SET, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SET_PARMS) lpSet
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

<span id="lpSet"></span><span id="lpset"></span><span id="LPSET"></span>*lpSet*
</dt> <dd>

Pointeur vers une [**structure \_ Set \_ PARMS de MCI**](mci-set-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge l' \_ ensemble MCI :

<dl> <dt>

<span id="MCI_SET_AUDIO"></span><span id="mci_set_audio"></span>MCI \_ définir le \_ son
</dt> <dd>

Un numéro de canal audio est inclus dans le membre dwAudio de la structure identifiée par *lpSet*. Cet indicateur doit être utilisé avec l’option MCI activée \_ \_ ou \_ activée \_ . Utilisez l’une des constantes suivantes pour indiquer le numéro de canal :

</dd> <dt>

<span id="MCI_SET_AUDIO_ALL"></span><span id="mci_set_audio_all"></span>MCI- \_ définir l' \_ audio \_ tout
</dt> <dd>

Tous les canaux audio.

</dd> <dt>

<span id="MCI_SET_AUDIO_LEFT"></span><span id="mci_set_audio_left"></span>MCI- \_ définir l' \_ audio à \_ gauche
</dt> <dd>

Canal gauche.

</dd> <dt>

<span id="MCI_SET_AUDIO_RIGHT"></span><span id="mci_set_audio_right"></span>MCI \_ - \_ définir \_ le son
</dt> <dd>

Canal droit.

</dd> <dt>

<span id="MCI_SET_DOOR_CLOSED"></span><span id="mci_set_door_closed"></span>porte de l' \_ ensemble MCI \_ \_ fermée
</dt> <dd>

Ferme le support multimédia (le cas échéant).

</dd> <dt>

<span id="MCI_SET_DOOR_OPEN"></span><span id="mci_set_door_open"></span>porte de l' \_ ensemble MCI \_ \_ ouverte
</dt> <dd>

Ouvre la couverture du support (le cas échéant).

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Désactive le canal vidéo ou audio spécifié.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Active le canal vidéo ou audio spécifié.

</dd> <dt>

<span id="MCI_SET_TIME_FORMAT"></span><span id="mci_set_time_format"></span>FORMAT d’heure de l' \_ ensemble MCI \_ \_
</dt> <dd>

Un paramètre de format d’heure est inclus dans le membre **dwTimeFormat** de la structure identifiée par *lpSet*. Les indicateurs suivants sont utilisés avec cet indicateur :

</dd> <dt>

<span id="MCI_FORMAT_BYTES"></span><span id="mci_format_bytes"></span>\_octets au format MCI \_
</dt> <dd>

Dans un format de données PCM (Pulse Code Modulation), modifie la description du membre de temps en octets pour l’entrée ou la sortie. Reconnu par le type d’appareil **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_FRAMES"></span><span id="mci_format_frames"></span>\_images au format MCI \_
</dt> <dd>

Les commandes suivantes utilisent des frames. Reconnu par les types d’appareils **Digitalvideo**, **VCR** et **videodisc** .

</dd> <dt>

<span id="MCI_FORMAT_HMS"></span><span id="mci_format_hms"></span>\_format MCI \_ HMS
</dt> <dd>

Modifie le format d’heure en heures, minutes et secondes. Reconnu par les types de périphérique **VCR** et **videodisc** .

</dd> <dt>

<span id="MCI_FORMAT_MILLISECONDS"></span><span id="mci_format_milliseconds"></span>FORMAT MCI en \_ \_ millisecondes
</dt> <dd>

Modifie le format d’heure en millisecondes. Reconnu par tous les types d’appareils.

</dd> <dt>

<span id="MCI_FORMAT_MSF"></span><span id="mci_format_msf"></span>FORMAT MCI ( \_ \_ MSF)
</dt> <dd>

Change le format d’heure en minutes, secondes et frames. Reconnu par les types d’appareils **cdaudio** et **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SAMPLES"></span><span id="mci_format_samples"></span>\_exemples de format MCI \_
</dt> <dd>

Remplace le format d’heure par des exemples d’entrée ou de sortie. Reconnu par le type d’appareil **WaveAudio** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__and_MCI_FORMAT_SMPTE_30"></span><span id="mci_format_smpte_24__mci_format_smpte_25__and_mci_format_smpte_30"></span><span id="MCI_FORMAT_SMPTE_24__MCI_FORMAT_SMPTE_25__AND_MCI_FORMAT_SMPTE_30"></span>\_Format MCI \_ SMPTE \_ 24, \_ format MCI \_ SMPTE \_ 25 et format MCI \_ , \_ SMPTE \_ 30
</dt> <dd>

Définit le format d’heure sur 24, 25 et 30 images SMPTE (société de mouvement et ingénieurs de télévision), respectivement. Reconnus par les types de périphérique **Sequencer** et **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_SMPTE_30DROP"></span><span id="mci_format_smpte_30drop"></span>\_Format MCI \_ \_ 30DROP SMPTE
</dt> <dd>

Définit le format d’heure sur 30 SMPTE de dépôt. Reconnus par les types de périphérique **Sequencer** et **VCR** .

</dd> <dt>

<span id="MCI_FORMAT_TMSF"></span><span id="mci_format_tmsf"></span>\_format MCI \_ TMSF
</dt> <dd>

Modifie le format d’heure en pistes, minutes, secondes et frames. (MCI utilise des numéros de pistes continus.) Reconnu par les types d’appareils **cdaudio** et **VCR** .

</dd> <dt>

<span id="MCI_SET_VIDEO"></span><span id="mci_set_video"></span>\_vidéo Set \_ MCI
</dt> <dd>

Définit le signal vidéo activé ou désactivé. Cet indicateur doit être utilisé avec l’option MCI activée ou l’option \_ \_ MCI \_ \_ désactivée. Les appareils qui n’ont pas de vidéo retournent une fonction MCIERR non \_ prise en charge \_ .

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_SET_FILEFORMAT"></span><span id="mci_dgv_set_fileformat"></span>MCI \_ DGV \_ Set \_ FILEFORMAT
</dt> <dd>

Un paramètre de format de fichier est inclus dans le membre **dwFileFormat** de la structure identifiée par *lpSet*. Pour les périphériques vidéo numériques, le format de fichier est utilisé pour les commandes d’enregistrement ou de capture. En cas d’omission, il peut s’agit d’un format défini par défaut pour le pilote de périphérique. Si le format de fichier spécifié est en conflit avec l’algorithme et la qualité actuellement sélectionnés, ils sont remplacés par les valeurs par défaut pour le format de fichier. Les constantes de format de fichier suivantes sont définies :

</dd> <dt>

<span id="MCI_DGV_FF_AVI"></span><span id="mci_dgv_ff_avi"></span>MCI \_ DGV \_ FF \_ AVI
</dt> <dd>

Format AVI.

</dd> <dt>

<span id="MCI_DGV_FF_AVSS"></span><span id="mci_dgv_ff_avss"></span>MCI \_ DGV \_ FF \_ avss
</dt> <dd>

Format AVSS.

</dd> <dt>

<span id="MCI_DGV_FF_DIB"></span><span id="mci_dgv_ff_dib"></span>MCI \_ DGV \_ FF \_ DIB
</dt> <dd>

Format DIB.

</dd> <dt>

<span id="MCI_DGV_FF_JFIF"></span><span id="mci_dgv_ff_jfif"></span>MCI \_ DGV \_ FF \_ JFIF
</dt> <dd>

Format JFIF.

</dd> <dt>

<span id="MCI_DGV_FF_JPEG"></span><span id="mci_dgv_ff_jpeg"></span>MCI \_ DGV \_ FF \_ JPEG
</dt> <dd>

Format JPEG.

</dd> <dt>

<span id="MCI_DGV_FF_MPEG"></span><span id="mci_dgv_ff_mpeg"></span>MCI \_ DGV \_ FF \_ MPEG
</dt> <dd>

Format MPEG.

</dd> <dt>

<span id="MCI_DGV_FF_RDIB"></span><span id="mci_dgv_ff_rdib"></span>MCI \_ DGV \_ FF \_ RDIB
</dt> <dd>

Format DIB RLE.

</dd> <dt>

<span id="MCI_DGV_FF_RJPEG"></span><span id="mci_dgv_ff_rjpeg"></span>MCI \_ DGV \_ FF \_ RJPEG
</dt> <dd>

Format RJPEG.

</dd> <dt>

<span id="MCI_DGV_SET_SEEK_EXACTLY"></span><span id="mci_dgv_set_seek_exactly"></span>configuration de la recherche MCI \_ DGV \_ \_ \_
</dt> <dd>

Définit le format utilisé pour le positionnement. Cet indicateur doit être utilisé avec l’option MCI activée \_ \_ ou \_ activée \_ . Si \_ l’option MCI activée \_ est spécifiée, la fonction de jeu ou d’enregistrement accède précisément à la trame spécifiée avec l' \_ indicateur MCI. Cela peut ajouter un délai supplémentaire si la trame demandée n’est pas une image clé. Si \_ la valeur \_ OFF est spécifiée pour MCI, l’appareil recherche une image d’image clé qui précède le frame demandé. Pour certains fichiers et périphériques, il peut s’agir de la première image du fichier. La valeur par défaut de cet indicateur dépend de l’appareil.

</dd> <dt>

<span id="MCI_DGV_SET_SPEED"></span><span id="mci_dgv_set_speed"></span>\_vitesse de \_ définition de DGV MCI \_
</dt> <dd>

Un paramètre de vitesse est inclus dans le membre **dwSpeed** de la structure identifiée par *lpSet*. La vitesse est spécifiée comme un ratio entre la fréquence d’images nominale et la fréquence d’images souhaitée où la fréquence d’images nominale est désignée comme 1000. Une demi-vitesse est de 500 et la double vitesse est de 2000. La plage de vitesse autorisée dépend également du périphérique et éventuellement du fichier.

</dd> <dt>

<span id="MCI_DGV_SET_STILL"></span><span id="mci_dgv_set_still"></span>\_jeu de DGV MCI \_ \_
</dt> <dd>

Lorsqu’il est utilisé avec MCI \_ DGV \_ Set \_ FILEFORMAT, MCI \_ Set définit le format de fichier utilisé pour les commandes de capture.

</dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpSet* pointe vers une structure [**MCI \_ DGV \_ Set \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_set_parms) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Sequencer** :

<dl> <dt>

<span id="MCI_SEQ_FORMAT_SONGPTR"></span><span id="mci_seq_format_songptr"></span>MCI \_ Seq \_ format \_ SONGPTR
</dt> <dd>

Définit le format d’heure sur les unités du pointeur de la chanson.

</dd> <dt>

<span id="MCI_SEQ_SET_MASTER"></span><span id="mci_seq_set_master"></span>\_contrôleur d’ensemble de séquences MCI \_ \_
</dt> <dd>

Définit Sequencer comme source de données de synchronisation et indique que le type de synchronisation est spécifié dans le membre **dwMaster** de la structure identifiée par *lpSet*. MCISEQ retourne une \_ fonction non prise en charge MCIERR \_ . Les constantes suivantes sont définies pour le type de synchronisation :

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ midi
</dt> <dd>

Sequencer enverra les données de synchronisation au format MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE
</dt> <dd>

Sequencer enverra les données de synchronisation au format SMPTE.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ aucun
</dt> <dd>

Sequencer n’enverra pas de données de synchronisation.

</dd> <dt>

<span id="MCI_SEQ_SET_OFFSET"></span><span id="mci_seq_set_offset"></span>décalage de l' \_ ensemble de séquences MCI \_ \_
</dt> <dd>

Remplace le décalage SMPTE d’une séquence par celui spécifié par le membre **dwOffset** de la structure identifiée par *lpSet*. Cela affecte uniquement les séquences avec un type de division SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_PORT"></span><span id="mci_seq_set_port"></span>\_port MCI Seq \_ Set \_
</dt> <dd>

Définit le port MIDI de sortie d’une séquence sur celui spécifié par l’identificateur d’appareil MIDI dans le membre **dwPort** de la structure identifiée par *lpSet*. L’appareil ferme le port précédent (le cas échéant) et tente d’ouvrir et d’utiliser le nouveau port. Si elle échoue, elle retourne une erreur et ouvre à nouveau le port précédemment utilisé (le cas échéant). Les constantes suivantes sont définies pour les ports :

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ aucun
</dt> <dd>

Ferme le port précédemment utilisé (le cas échéant). Sequencer se comporte exactement comme si un port était ouvert, à l’exception du fait qu’aucun message MIDI n’est envoyé.

</dd> <dt>

<span id="MIDI_MAPPER"></span><span id="midi_mapper"></span>\_Mappeur midi
</dt> <dd>

Définit le port ouvert sur le Mappeur MIDI.

</dd> <dt>

<span id="MCI_SEQ_SET_SLAVE"></span><span id="mci_seq_set_slave"></span>MCI \_ Seq \_ Set \_ esclave
</dt> <dd>

Définit Sequencer pour recevoir des données de synchronisation et indique que le type de synchronisation est spécifié dans le membre **dwSlave** de la structure identifiée par *lpSet*. MCISEQ retourne une \_ fonction non prise en charge MCIERR \_ . Les constantes suivantes sont définies pour le type de synchronisation :

</dd> <dt>

<span id="MCI_SEQ_FILE"></span><span id="mci_seq_file"></span>\_fichier séquence \_ MCI
</dt> <dd>

Définit le séquenceur pour qu’il reçoive les données de synchronisation contenues dans le fichier MIDI.

</dd> <dt>

<span id="MCI_SEQ_MIDI"></span><span id="mci_seq_midi"></span>MCI \_ Seq \_ midi
</dt> <dd>

Définit le séquenceur pour qu’il reçoive les données de synchronisation MIDI.

</dd> <dt>

<span id="MCI_SEQ_NONE"></span><span id="mci_seq_none"></span>MCI \_ Seq \_ aucun
</dt> <dd>

Définit le Sequencer pour qu’il ignore les données de synchronisation dans un flux MIDI.

</dd> <dt>

<span id="MCI_SEQ_SMPTE"></span><span id="mci_seq_smpte"></span>MCI \_ Seq \_ SMPTE
</dt> <dd>

Définit le séquenceur pour qu’il reçoive les données de synchronisation SMPTE.

</dd> <dt>

<span id="MCI_SEQ_SET_TEMPO"></span><span id="mci_seq_set_tempo"></span>\_tempo d’ensemble de séquences MCI \_ \_
</dt> <dd>

Remplace le tempo de la séquence MIDI par celui spécifié par le membre **dwTempo** de la structure vers laquelle pointe *lpSet*. Pour les séquences avec le type de division PPQN, le tempo est spécifié en temps par minute. pour les séquences avec le type de division SMPTE, le tempo est spécifié en images par seconde.

</dd> </dl>

Pour les appareils Sequencer, le paramètre *lpSet* pointe vers une structure [**MCI \_ Seq \_ Set \_ PARMS**](mci-seq-set-parms.md) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_SET_ASSEMBLE_RECORD"></span><span id="mci_vcr_set_assemble_record"></span>\_jeu d' \_ \_ enregistrements d’assemblage de magnétoscope MCI \_
</dt> <dd>

Définit l’appareil à enregistrer dans les modes assembleur ou insertion (lorsque l’option assembler est désactivée, l’insertion est activée et vice versa). Utilisez avec l’un des indicateurs suivants :

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Définit l’enregistrement d’assemblage sur et désactive l’enregistrement d’insertion. Enregistre toutes les pistes vidéo, audio et de code temporel.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Définit l’enregistrement d’assemblage OFF et active l’enregistrement d’insertion sur. Lorsque l’option assembler l’enregistrement est désactivée, les pistes individuelles de la vidéo, de l’audio et du code temporel peuvent être sélectionnées pour l’enregistrement.

</dd> <dt>

<span id="MCI_VCR_SET_CLOCK"></span><span id="mci_vcr_set_clock"></span>\_horloge du jeu de magnétoscopes MCI \_ \_
</dt> <dd>

Le membre **dwClock** de la structure identifiée par *lpSet* contient la nouvelle heure de l’horloge.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_FORMA"></span><span id="mci_vcr_set_counter_forma"></span>\_format du \_ compteur de jeu de magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwCounterFormat** de la structure identifiée par *lpSet* contient une constante qui spécifie le nouveau format de compteur à utiliser par le compteur d’État. Pour obtenir la liste des constantes valides, \_ consultez \_ format d’heure Set MCI \_ dans la liste des indicateurs supplémentaires pour cette commande.

</dd> <dt>

<span id="MCI_VCR_SET_COUNTER_VALUE"></span><span id="mci_vcr_set_counter_value"></span>valeur du compteur de l' \_ ensemble de magnétoscopes MCI \_ \_ \_
</dt> <dd>

Le membre **dwCounterValue** de la structure identifiée par *lpSet* contient la nouvelle valeur de compteur.

</dd> <dt>

<span id="MCI_VCR_SET_INDEX"></span><span id="mci_vcr_set_index"></span>\_jeu d' \_ \_ index magnétoscope MCI
</dt> <dd>

Le membre **dwIndex** de la structure identifiée par *lpSet* contient une constante indiquant le contenu de l’affichage à l’écran et doit être l’un des éléments suivants :

</dd> <dt>

<span id="MCI_VCR_INDEX_COUNTER"></span><span id="mci_vcr_index_counter"></span>\_compteur d' \_ index \_ magnétoscope MCI
</dt> <dd>

Affiche le compteur.

</dd> <dt>

<span id="MCI_VCR_INDEX_DATE"></span><span id="mci_vcr_index_date"></span>\_Date d' \_ index \_ magnétoscope MCI
</dt> <dd>

Affiche la date.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIME"></span><span id="mci_vcr_index_time"></span>\_heure d' \_ index \_ magnétoscope MCI
</dt> <dd>

Affiche l’heure.

</dd> <dt>

<span id="MCI_VCR_INDEX_TIMECODE"></span><span id="mci_vcr_index_timecode"></span>\_code temporel de l’index magnétoscope MCI \_ \_
</dt> <dd>

Affiche le code temporel.

Pour plus d’informations, consultez la commande d' [ \_ index MCI](mci-index.md) .

</dd> <dt>

<span id="MCI_VCR_SET_PAUSE_TIMEOUT"></span><span id="mci_vcr_set_pause_timeout"></span>\_délai de \_ \_ pause \_ du jeu de magnétoscope MCI
</dt> <dd>

Le membre **dwPauseTimeout** de la structure identifiée par *lpSet* contient la durée maximale, en millisecondes, d’une commande pause.

</dd> <dt>

<span id="MCI_VCR_SET_POSTROLL_DURATION"></span><span id="mci_vcr_set_postroll_duration"></span>durée de l' \_ ensemble des magnétoscopes MCI \_ \_ \_
</dt> <dd>

Le membre **dwPostrollDuration** de la structure identifiée par *lpSet* contient la longueur des cassettes vidéo, au format de l’heure actuelle, nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande Stop ou pause.

</dd> <dt>

<span id="MCI_VCR_SET_POWER"></span><span id="mci_vcr_set_power"></span>\_alimentation du jeu de magnétoscopes MCI \_ \_
</dt> <dd>

Définit la mise sous tension ou la désactivation. Doit être utilisé avec l’un des indicateurs suivants :

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Désactive l’alimentation.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Active la mise sous tension.

</dd> <dt>

<span id="MCI_VCR_SET_PREROLL_DURATION"></span><span id="mci_vcr_set_preroll_duration"></span>\_durée du \_ préroll du jeu de magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwPrerollDuration** de la structure identifiée par *lpSet* contient la longueur des cassettes vidéo, au format de l’heure actuelle, nécessaire pour stabiliser la sortie du magnétoscope.

</dd> <dt>

<span id="MCI_VCR_SET_RECORD_FORMAT"></span><span id="mci_vcr_set_record_format"></span>\_format d' \_ enregistrement du jeu de magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwRecordFormat** de la structure identifiée par *lpSet* contient une constante décrivant la vitesse des enregistrements, qui doit être l’une des suivantes :

</dd> <dt>

<span id="MCI_VCR_FORMAT_EP"></span><span id="mci_vcr_format_ep"></span>\_format VCR \_ MCI \_ EP
</dt> <dd>

Enregistrements à vitesse lente.

</dd> <dt>

<span id="MCI_VCR_FORMAT_LP"></span><span id="mci_vcr_format_lp"></span>\_format de magnétoscope MCI \_ \_ LP
</dt> <dd>

Enregistrements à vitesse moyenne lente.

</dd> <dt>

<span id="MCI_VCR_FORMAT_SP"></span><span id="mci_vcr_format_sp"></span>MCI \_ magnétoscope \_ au format \_ SP
</dt> <dd>

Enregistrements à la vitesse standard.

</dd> <dt>

<span id="MCI_VCR_SET_SPEED"></span><span id="mci_vcr_set_speed"></span>\_ \_ vitesse définie pour magnétoscope MCI \_
</dt> <dd>

Le membre **dwSpeed** de la structure identifiée par *lpSet* contient le nouveau paramètre de vitesse, où 1000 correspond à la vitesse normale, 2000 à la vitesse et 500 à mi-vitesse, et ainsi de suite.

</dd> <dt>

<span id="MCI_VCR_SET_TAPE_LENGTH"></span><span id="mci_vcr_set_tape_length"></span>\_longueur de \_ bande du jeu de MAGNÉTOSCOPEs MCI \_ \_
</dt> <dd>

Le membre **dwTapeLength** de la structure identifiée par *lpSet* contient la nouvelle longueur de la bande, à condition que la longueur de la bande ne soit pas détectable.

</dd> <dt>

<span id="MCI_VCR_SET_TIME_MODE"></span><span id="mci_vcr_set_time_mode"></span>magnétoscope MCI- \_ \_ définir le \_ \_ mode temporel
</dt> <dd>

Le membre **dwTimeMode** de la structure identifiée par *lpSet* contient une constante indiquant le nouveau mode de temps de position. Les constantes suivantes sont valides :

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_compteur de \_ temps MCI VCR \_
</dt> <dd>

Force l’appareil à utiliser le compteur exclusivement.

</dd> <dt>

<span id="MCI_VCR_TIME_DETECT"></span><span id="mci_vcr_time_detect"></span>détection de l' \_ heure du magnétoscope MCI \_ \_
</dt> <dd>

Chaque fois qu’une nouvelle bande vidéo est insérée dans l’appareil ou que le mode passe de non prêt à prêt, l’appareil doit tenter de déterminer si un code temporel est disponible sur la bande vidéo. Si le code temporel est disponible, utilisez le code temporel dans toutes les commandes suivantes qui spécifient des positions. Dans le cas contraire, utilisez le compteur.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_code temporel de l’heure MCI magnétoscope \_ \_
</dt> <dd>

Force l’appareil à utiliser le code temporel exclusivement.

</dd> <dt>

<span id="MCI_VCR_SET_TRACKING"></span><span id="mci_vcr_set_tracking"></span>\_suivi du jeu de magnétoscopes MCI \_ \_
</dt> <dd>

Ajuste la vitesse du transport de bande VCR avec un ajustement précis et doit être utilisé avec l’un des indicateurs suivants :

</dd> <dt>

<span id="MCI_VCR_PLUS"></span><span id="mci_vcr_plus"></span>\_magnétoscope MCI \_ plus
</dt> <dd>

Augmente la vitesse de transport de bande.

</dd> <dt>

<span id="MCI_VCR_MINUS"></span><span id="mci_vcr_minus"></span>\_magnétoscope MCI \_ moins
</dt> <dd>

Diminue la vitesse du transport sur bande.

</dd> <dt>

<span id="MCI_VCR_RESET"></span><span id="mci_vcr_reset"></span>\_réinitialisation de magnétoscope MCI \_
</dt> <dd>

Retourne l’ajustement de suivi à zéro.

</dd> </dl>

Pour les périphériques VCR, le paramètre *lpSet* pointe vers une structure d' [**\_ \_ ensemble \_ de magnétoscopes MCI**](mci-vcr-set-parms.md) .

L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **videodisc** :

<dl> <dt>

<span id="MCI_VD_FORMAT_TRACK"></span><span id="mci_vd_format_track"></span>\_piste de \_ format MCI VD \_
</dt> <dd>

Modifie le format d’heure en pistes. MCI utilise des numéros de pistes continus.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_
</dt> <dd>

Définit l’entrée utilisée pour l’enregistrement dans le membre **wInput** de la structure identifiée par *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_
</dt> <dd>

Définit la sortie utilisée pour la diffusion dans le membre **wOutput** de la structure identifiée par *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYINPUT"></span><span id="mci_wave_set_anyinput"></span>\_jeu Wave \_ MCI \_ ANYINPUT
</dt> <dd>

Toutes les entrées Wave compatibles avec le format actuel peuvent être utilisées pour l’enregistrement.

</dd> <dt>

<span id="MCI_WAVE_SET_ANYOUTPUT"></span><span id="mci_wave_set_anyoutput"></span>\_jeu Wave \_ MCI \_ ANYOUTPUT
</dt> <dd>

Toutes les sorties Wave compatibles avec le format actuel peuvent être utilisées pour la diffusion.

</dd> <dt>

<span id="MCI_WAVE_SET_AVGBYTESPERSEC"></span><span id="mci_wave_set_avgbytespersec"></span>\_jeu Wave \_ MCI \_ AVGBYTESPERSEC
</dt> <dd>

Définit le nombre d’octets par seconde utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nAvgBytesPerSec** de la structure identifiée par *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BITSPERSAMPLE"></span><span id="mci_wave_set_bitspersample"></span>\_jeu Wave \_ MCI \_ BitsPerSample
</dt> <dd>

Définit le nombre de bits par échantillon utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nBitsPerSample** du format de données PCM identifié par *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_BLOCKALIGN"></span><span id="mci_wave_set_blockalign"></span>\_jeu Wave \_ MCI \_ BLOCKALIGN
</dt> <dd>

Définit l’alignement de bloc utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nBlockAlign** de la structure identifiée par *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_CHANNELS"></span><span id="mci_wave_set_channels"></span>\_canaux de \_ jeu \_ Wave MCI
</dt> <dd>

Le nombre de canaux est indiqué dans le membre **nChannels** de la structure identifiée par *lpSet*.

</dd> <dt>

<span id="MCI_WAVE_SET_FORMATTAG"></span><span id="mci_wave_set_formattag"></span>\_jeu Wave \_ MCI \_ FORMATTAG
</dt> <dd>

Définit le type de format utilisé pour la diffusion, l’enregistrement et l’enregistrement dans le membre **wFormatTag** de la structure identifiée par *lpSet*. La spécification \_ du format Wave \_ PCM change le format en PCM.

</dd> <dt>

<span id="MCI_WAVE_SET_SAMPLESPERSEC"></span><span id="mci_wave_set_samplespersec"></span>\_jeu Wave \_ MCI \_ SAMPLESPERSEC
</dt> <dd>

Définit les échantillons par seconde utilisés pour la diffusion, l’enregistrement et l’enregistrement dans le membre **nSamplesPerSec** de la structure identifiée par *lpSet*.

</dd> </dl>

Pour les périphériques audio Waveform, le paramètre *lpSet* pointe vers une structure de paramètres [**\_ Wave \_ \_ MCI**](mci-wave-set-parms.md) .

Plusieurs propriétés des données Waveform-Audio sont définies lors de la création du fichier de stockage des données. Ces propriétés décrivent comment les données sont structurées dans le fichier et ne peuvent pas être modifiées une fois l’enregistrement commencé. La liste d’indicateurs suivante identifie ces propriétés :

-   \_jeu Wave \_ MCI \_ AVGBYTESPERSEC
-   \_jeu Wave \_ MCI \_ BitsPerSample
-   \_jeu Wave \_ MCI \_ BLOCKALIGN
-   \_canaux de \_ jeu \_ Wave MCI
-   \_jeu Wave \_ MCI \_ FORMATTAG
-   \_jeu Wave \_ MCI \_ SAMPLESPERSEC

## <a name="requirements"></a>Conditions requises



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

 

