---
title: Commande MCI_SETAUDIO (mmsystem. h)
description: La \_ commande MCI SETAUDIO définit les valeurs associées à la lecture et à la capture audio. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- commande MCI_SETAUDIO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882209b8a9debc2c01e4f5c6f852d418c1a5cd321a764af022d19c58fe32a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803396"
---
# <a name="mci_setaudio-command"></a>\_Commande MCI SETAUDIO

La \_ commande MCI SETAUDIO définit les valeurs associées à la lecture et à la capture audio. Les appareils vidéo numériques et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
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

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs suivants s’appliquent au type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>MCI \_ DGV \_ SETAUDIO \_ ALG
</dt> <dd>

Le membre **lpstrAlgorithm** de la structure identifiée par *lpSetAudio* contient l’adresse d’une mémoire tampon contenant le nom d’un algorithme de compression audio. L’algorithme de compression est utilisé par les commandes de [ \_ réserve MCI](mci-reserve.md) ou d' [ \_ enregistrement MCI](mci-record.md) suivantes. Les algorithmes disponibles dépendent du périphérique. Si l’algorithme est incompatible avec le format de fichier actuel, le format de fichier est remplacé par le format par défaut de l’algorithme.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>MCI \_ DGV \_ SETAUDIO \_ CLOCKTIME
</dt> <dd>

L’heure spécifiée est exprimée en millisecondes et est l’heure absolue quand elle est utilisée avec MCI \_ DGV \_ SETAUDIO \_ . (Cette heure n’est pas à l’étape de la diffusion de l’espace de travail.)

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_entrée MCI DGV \_ SETAUDIO \_
</dt> <dd>

Modifie l’indicateur Bass, aigus ou volume pour qu’il affecte le signal d’entrée et modifie ce qui est enregistré. Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_ \_ élément SETAUDIO DGV \_ MCI
</dt> <dd>

Une constante audio est spécifiée dans le membre **dwItem** de la structure identifiée par *lpSetAudio*. La constante identifie la valeur qui est définie. Les constantes suivantes sont définies :

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>MCI \_ DGV \_ SETAUDIO \_ AVGBYTESPERSEC
</dt> <dd>

Le nombre moyen d’octets est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. Cette valeur définit le nombre moyen d’octets par seconde pour la diffusion ou l’enregistrement dans les formats PCM (Pulse Code Modulation) et ADPCM (Adaptive Differential Pulse Code Modulation). Le fichier est enregistré dans ce format.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SETAUDIO \_ Bass
</dt> <dd>

Le niveau de fréquence basse audio est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>MCI \_ DGV \_ SETAUDIO \_ BitsPerSample
</dt> <dd>

Le nombre de bits par échantillon est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. Cette valeur définit le nombre de bits par échantillon lu ou enregistré au format PCM. Le fichier est enregistré dans ce format.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>MCI \_ DGV \_ SETAUDIO \_ BLOCKALIGN
</dt> <dd>

L’alignement du bloc de données est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. Cette valeur définit l’alignement des blocs de données par rapport au début des données de forme d’onde en entrée.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>MCI \_ DGV \_ SETAUDIO \_ SAMPLESPERSEC
</dt> <dd>

Le taux d’échantillonnage est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. Cette valeur définit le taux d’échantillonnage pour la diffusion et l’enregistrement avec les algorithmes PCM et ADPCM. Le fichier est enregistré dans ce format.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_source MCI DGV \_ SETAUDIO \_
</dt> <dd>

Une constante qui spécifie la source d’entrée audio est incluse dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. Les constantes suivantes sont définies pour les sources d’entrée audio :

moyenne de la \_ source MCI DGV \_ SETAUDIO \_ \_

Moyenne des canaux audio de gauche et de droite.

\_ \_ source SETAUDIO DGV \_ MCI \_

Canal audio de gauche.

\_DGV \_ SETAUDIO \_ source \_ MCI

Canal audio approprié.

\_ \_ \_ stéréo source SETAUDIO DGV \_ MCI

Enceintes.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_flux MCI DGV \_ SETAUDIO \_
</dt> <dd>

Un flux audio est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. La valeur entière spécifie le flux audio lu à partir de l’espace de travail. Si le flux n’est pas spécifié, le premier flux audio entrelacé physiquement est lu.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>\_DGV MCI \_ SETAUDIO \_ aigus
</dt> <dd>

Le niveau haute fréquence audio est spécifié comme un facteur dans le membre **dwValue** de la structure identifiée par *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_ \_ volume SETAUDIO DGV \_ MCI
</dt> <dd>

Le niveau audio d’un ou des deux canaux audio est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. Si les volumes de gauche et de droite ont été définis sur des valeurs différentes, le rapport entre le volume de gauche et le volume de droite est approximativement inchangé.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ gauche
</dt> <dd>

Active le canal audio de gauche lorsqu’il est utilisé avec MCI activé \_ \_ . Désactive le canal audio de gauche lorsqu’il est utilisé avec \_ MCI \_ désactivé. Lorsque cet indicateur est utilisé avec la combinaison de la \_ \_ valeur SETAUDIO MCI DGV \_ et du \_ volume MCI DGV \_ SETAUDIO \_ , il définit le volume du canal audio de gauche. Lorsque cet indicateur est utilisé avec la \_ source MCI DGV \_ SETAUDIO \_ , il spécifie le canal audio de gauche comme source pour le numériseur d’entrée audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ SETAUDIO \_
</dt> <dd>

Un paramètre de longueur de transition est inclus dans le membre **dwOver** de la structure identifiée par *lpSetAudio*. La valeur de longueur spécifie la durée (en unités du format d’heure actuel) à effectuer pour effectuer une modification qui utilise un facteur. Si cet indicateur n’est pas utilisé, les modifications se produisent immédiatement.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_DGV MCI \_ SETAUDIO \_
</dt> <dd>

Le membre **lpstrQuality** de la structure identifiée par *lpSetAudio* contient l’adresse d’une mémoire tampon définissant la qualité audio. Une chaîne de texte dans la mémoire tampon spécifie les caractéristiques de l’algorithme de compression audio.

L' \_ indicateur MCI DGV \_ SETAUDIO \_ ALG peut être utilisé pour sélectionner un descripteur de qualité pour l’algorithme spécifié. Si cet indicateur est omis, l’algorithme actuel est utilisé.

Les algorithmes et les noms de descripteurs disponibles dépendent du périphérique. Chaque appareil fournit de la documentation pour les algorithmes disponibles et une description des noms de descripteur applicables. La commande [MCI \_ Quality](mci-quality.md) peut définir des noms de descripteurs supplémentaires.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_enregistrement MCI DGV \_ SETAUDIO \_
</dt> <dd>

Spécifie si l’enregistrement inclut ou exclut les données audio. Lorsqu’elles sont combinées avec MCI activé \_ \_ , les données audio sont enregistrées. Lorsqu’elle est associée à l' \_ option MCI activée \_ , les données audio sont exclues. La valeur par défaut comprend les données audio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ Right
</dt> <dd>

Active le canal audio approprié lorsqu’il est utilisé avec MCI activé \_ \_ . Désactive le canal audio approprié lorsqu’il est utilisé avec MCI \_ \_ désactivé. Lorsque cet indicateur est utilisé avec la combinaison de la \_ \_ valeur SETAUDIO MCI DGV \_ et du \_ volume MCI DGV \_ SETAUDIO \_ , il définit le volume du canal audio approprié.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_ \_ valeur SETAUDIO de DGV MCI \_
</dt> <dd>

Une valeur est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetAudio*. La signification de la valeur est spécifiée par la constante définie pour l’indicateur de l' \_ \_ élément SETAUDIO MCI DGV \_ .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Désactive le canal audio spécifié.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Active le canal audio spécifié.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>\_sortie MCI SETAUDIO \_
</dt> <dd>

Modifie l’indicateur Bass, aigus ou volume afin qu’il modifie uniquement le signal joué et non ce qui est enregistré. Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpSetAudio* pointe vers une structure [**MCI \_ DGV \_ SETAUDIO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_ \_ enregistrement SETAUDIO magnétoscope \_ MCI
</dt> <dd>

Définit l’enregistrement audio sur on ou OFF, qui est utilisé conjointement avec l’un des indicateurs suivants :

MCI \_ activé \_

Enregistrement audio activé.

MCI \_ \_ désactivé

Enregistrement audio désactivé. Il peut être nécessaire de désactiver d’abord l’enregistrement de l’assembly (à l’aide de la commande [ \_ Set MCI](mci-set.md) avec l’indicateur de l' \_ \_ \_ enregistrement assembler de l’ensemble magnétoscope MCI \_ défini sur OFF) avant que l’enregistrement audio puisse être désactivé.

\_piste MCI

Le membre **dwTrack** de la structure identifiée par *lpSetAudio* spécifie la piste qui est affectée par la commande.

\_ \_ source SETAUDIO magnétoscope \_ MCI

Définit la source audio. Cet indicateur doit être utilisé avec le \_ magnétoscope MCI \_ SETAUDIO \_ pour signaler.

\_ \_ moniteur SETAUDIO magnétoscope \_ MCI

Définit le moniteur de la source audio. Cet indicateur doit être utilisé avec le \_ magnétoscope MCI \_ SETAUDIO \_ pour signaler.

\_magnétoscope MCI \_ SETAUDIO \_ à

Le membre **dwTo** de la structure identifiée par *lpSetAudio* contient une constante décrivant le type d’entrée ou d’entrée analysée. Il doit s’agir de l’un des éléments suivants :

<dl> <dd>

\_tuner de \_ \_ type SRC magnétoscope MCI \_

Type tuner.

</dd> <dd>

\_ligne de \_ \_ type SRC magnétoscope MCI \_

Le type est Line.

</dd> <dd>

\_magnétoscope MCI \_ type de source \_ \_ aux

Le type est auxiliaire.

</dd> <dd>

\_type de source de magnétoscope MCI \_ \_ \_ générique

Le type est Generic.

</dd> <dd>

\_type de source de magnétoscope MCI \_ \_ \_ muet

Le type est muet. Cela ne peut être utilisé qu’avec l' \_ indicateur de source MCI VCR \_ SETAUDIO \_ .

</dd> <dd>

\_sortie de \_ \_ type SRC magnétoscope MCI \_

Le type est output.

</dd> <dd>

\_ \_ numéro SETAUDIO magnétoscope \_ MCI

Le membre dwNumber de la structure identifiée par lpSetAudio contient l’entrée audio (du type spécifié dans le membre dwTo) à utiliser.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Pour les périphériques VCR, le paramètre *lpSetAudio* pointe vers une structure [**MCI \_ VCR \_ SETAUDIO \_ PARMS**](mci-vcr-setaudio-parms.md) .

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

 

