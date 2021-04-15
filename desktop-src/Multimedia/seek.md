---
title: commande Seek
description: La commande Seek passe à la position spécifiée et s’arrête. Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- commande Seek Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383924"
---
# <a name="seek-command"></a>commande Seek

La commande Seek passe à la position spécifiée et s’arrête. Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*
</dt> <dd>

Indicateur de déplacement à une position spécifiée. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Seek** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                          | Signification                      |
|--------------|----------------------------------|------------------------------|
| cdaudio      | fin jusqu’à la *position*             | pour démarrer                     |
| digitalvideo | fin jusqu’à la *position*             | pour démarrer                     |
| sequencer    | fin jusqu’à la *position*             | pour démarrer                     |
| vidéo          | à l' *instant*, marque *\_ num* inversé | fin jusqu’à la *position* de départ |
| videodisc    | inverser jusqu’à la fin                   | pour *positionner* pour démarrer        |
| WaveAudio    | fin jusqu’à la *position*             | pour démarrer                     |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszSeekFlags** et leurs significations.



| Valeur            | Signification                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| à *temps*        | Indique quand l’appareil doit commencer à exécuter cette commande ou, si l’appareil a été reçu, lorsque la commande de signal démarre. Pour plus d’informations, consultez la commande [CUE](cue.md) .                             |
| marque de marque *\_ num* | Recherche la marque relative indiquée par *Mark \_ num*, qui doit être une valeur entière positive. Les marques sont des signaux écrits sur la bande VCR à l’aide de la commande [Mark](mark.md) et sont utilisés pour une recherche rapide. |
| reverse          | Indique que la direction de la recherche sur les magnétoscopes et CAV videodiscs est vers l’arrière. Cet indicateur n’est pas valide si l’indicateur « to » est spécifié. Pour les magnétoscopes, cet indicateur doit être utilisé avec l’indicateur « Mark ».                             |
| pour terminer           | Recherche jusqu’à la fin du contenu.                                                                                                                                                                                 |
| pour *positionner*    | Spécifie la position d’arrêt de la recherche. Pour les appareils **cdaudio** , MCI retourne une erreur hors limites si la position spécifiée est supérieure à la longueur du disque.                                            |
| pour démarrer         | Recherche le début du contenu.                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .

Les périphériques vidéo numériques prennent en charge deux modes de recherche, que vous pouvez modifier à l’aide de la commande [Set](set.md) . Le mode « Seek exact on » provoque le déplacement de la commande Seek vers le frame spécifié. Le mode « Seek exact OFF » provoque le déplacement de la commande Seek vers l’image clé la plus proche avant le frame spécifié.

Si un périphérique CD audio est lu lors de l’émission de la commande Seek, la lecture est arrêtée. Lorsque la commande Seek est exécutée avec un appareil videodisc, l’appareil recherche à l’aide d’une avance rapide ou d’une inversion rapide avec la vidéo et l’audio.

Lorsque la commande Seek est émise avec un périphérique Wave-audio, le comportement dépend de la taille de l’échantillon. Si la taille de l’échantillon est supérieure ou égale à 16 bits, la fonction Seek se déplace au début de l’échantillon le plus proche lorsqu’une position spécifiée ne coïncide pas avec le début d’un exemple.

## <a name="examples"></a>Exemples

La commande suivante recherche le début du fichier multimédia associé à l’appareil « mySound ».

``` syntax
seek mysound to start
```

## <a name="requirements"></a>Configuration requise



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

[marque](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

