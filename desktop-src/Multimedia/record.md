---
title: enregistrer, commande
description: La commande d’enregistrement démarre l’enregistrement des données. Les périphériques VCR et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- commande enregistrer Windows multimédia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363911"
---
# <a name="record-command"></a>enregistrer, commande

La commande d’enregistrement démarre l’enregistrement des données. Les périphériques VCR et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

Indicateur pour l’enregistrement des données. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande d' **enregistrement** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                | Signification                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | *à partir du* *rectangle* flux audio Stream à partir de la *position* Hold | Insérer l’écrasement du *flux* de flux vidéo de la *position* |
| sequencer    | à partir de la *position* Insert                                  | remplacer la *position*                             |
| vidéo          | à l' *heure* de l’initialisation de la *position*                     | Insérer le remplacement à la *position*                      |
| WaveAudio    | à partir de la *position* Insert                                  | remplacer la *position*                             |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRecordFlags** et leurs significations.



| Valeur                 | Signification                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle*        | Spécifie une zone rectangulaire de l’entrée externe utilisée comme source pour les pixels compressés et enregistrés. S’il n’est pas spécifié, le rectangle est par défaut le rectangle spécifié pour [put](put.md) « Video ». Lorsqu’il est défini différemment du rectangle « Video », l’image affichée n’est pas ce qui est enregistré. |
| à *temps*             | Indique quand l’appareil doit commencer à exécuter cette commande ou, si l’appareil a été reçu, lorsque la commande de signal démarre. Pour plus d’informations, consultez la commande [CUE](cue.md) .                                                                                                                             |
| *flux* de flux audio | Spécifie le flux audio utilisé pour l’enregistrement. Si cet indicateur n’est pas spécifié et que le format de fichier ne définit pas de valeur par défaut, il est enregistré dans le flux qui est physiquement en premier.                                                                                                                             |
| à partir de la *position*       | Spécifie une position de départ pour l’enregistrement. Si l’indicateur « from » n’est pas spécifié, l’appareil commence à enregistrer à la position actuelle.                                                                                                                                                                       |
| inaltérable                  | Fige l’image lorsque l’enregistrement est terminé au lieu d’en visualiser la vidéo en direct. Lorsque l’enregistrement s’arrête, une commande de « fichier » d' [analyse](monitor.md) automatique est exécutée. Pour revenir à la vidéo en direct, émettez la commande « entrée » du **moniteur** .                                                                              |
| initialize            | Initialisez la bande (support), qui implique l’enregistrement du code temporel (si possible) pour la vidéo et l’audio vides. Cette commande peut prendre plusieurs heures si la bande entière doit être initialisée.                                                                                                                            |
| insert                | Spécifie que les nouvelles données sont ajoutées au fichier à la position actuelle.                                                                                                                                                                                                                                            |
| overwrite             | Spécifie que les nouvelles données remplacent les données dans le fichier.                                                                                                                                                                                                                                                           |
| pour *positionner*         | Spécifie une position de fin pour l’enregistrement. Si l’indicateur « to » n’est pas spécifié, l’appareil enregistre jusqu’à ce qu’il reçoive une commande [Stop](stop.md) ou [Pause](pause.md) .                                                                                                                                        |
| *flux* de flux vidéo | Spécifie le flux vidéo utilisé pour l’enregistrement. Si ce paramètre n’est pas spécifié et que le format de fichier ne définit pas de valeur par défaut, il est enregistré dans le flux qui est physiquement en premier.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

L’enregistrement s’arrête lorsqu’une commande [Stop](stop.md) ou [Pause](pause.md) est émise. Pour le pilote MCIWAVE, toutes les données enregistrées après l’ouverture d’un fichier sont ignorées si le fichier est fermé sans l’enregistrer.

Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) . Les pistes à enregistrer sont spécifiées par l' [settimecode](settimecode.md) « enregistrement », définissez les commandes « assembler l’enregistrement », [setvideo](setvideo.md) « enregistrement » et « enregistrement » de [SetAudio](setaudio.md) .

## <a name="examples"></a>Exemples

La commande suivante démarre l’enregistrement à la position actuelle.

``` syntax
record mysound
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[signal](cue.md)
</dt> <dt>

[socle](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[posé](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

