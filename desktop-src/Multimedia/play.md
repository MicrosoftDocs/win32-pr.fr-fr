---
title: commande Play
description: La commande Play démarre la lecture d’un appareil. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- commande Play Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509096"
---
# <a name="play-command"></a>commande Play

La commande Play démarre la lecture d’un appareil. Les périphériques CD audio, Digital-Video, MIDI Sequencer, videodisc, VCR et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Indicateur de la façon dont un appareil est lu. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Play** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                          | Signification                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | à partir de la *position*                  | pour *positionner*                     |
| digitalvideo | à partir de la *position* plein écran | inverser la fenêtre *position*       |
| sequencer    | à partir de la *position*                  | pour *positionner*                     |
| vidéo          | à l' *heure* de la *position* inverse  | analyser jusqu’au *poste*                |
| videodisc    | analyse inversée rapide à partir de la *position* | *entier* vitesse lente à *positionner* |
| WaveAudio    | à partir de la *position*                  | pour *positionner*                     |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszPlayFlags** et leurs significations.



| Valeur           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| à *temps*       | Indique quand l’appareil doit commencer à exécuter cette commande ou, si l’appareil a été reçu, lorsque la commande de signal démarre. Pour plus d’informations, consultez la commande [CUE](cue.md) .                                                                                                                                                                                                                                                                 |
| fast            | Indique que la lecture de l’appareil doit être plus rapide que la normale. Pour déterminer la vitesse exacte sur un lecteur videodisc, utilisez l’indicateur « Speed » de la commande [Status](status.md) . Pour spécifier la vitesse plus précisément, utilisez l’indicateur « Speed » de cette commande.                                                                                                                                                                                                   |
| à partir de la *position* | Spécifie une position de départ pour la lecture. Si l’indicateur « from » n’est pas spécifié, la lecture commence à la position actuelle. Pour les appareils **cdaudio** , si la position « de » est supérieure à la position de fin du disque, ou si la position « de » est supérieure à la position « à », le pilote retourne une erreur. Pour les appareils **videodisc** , les positions par défaut se trouvent dans des frames pour les disques CAV et en heures, minutes et secondes pour les disques CLV. |
| large      | Spécifie qu’un affichage plein écran doit être utilisé. Utilisez cet indicateur uniquement lors de la diffusion de fichiers compressés. (Les fichiers non compressés ne s’affichent pas en mode plein écran.)                                                                                                                                                                                                                                                                                                  |
| répéter          | Spécifie que la lecture doit redémarrer lorsque la fin du contenu est atteinte.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Spécifie que le sens de lecture est vers l’arrière. Vous ne pouvez pas spécifier un emplacement de fin avec l’indicateur « inversée ». Pour videodiscs, « Scan » s’applique uniquement au format CAV.                                                                                                                                                                                                                                                                                     |
| vérifier            | S’exécute aussi rapidement que possible sans désactiver la vidéo (même si l’audio est peut-être désactivé). Pour videodiscs, « Scan » s’applique uniquement au format CAV.                                                                                                                                                                                                                                                                                                             |
| slow            | La lecture est lente. Pour déterminer la vitesse exacte sur un lecteur videodisc, utilisez l’indicateur « Speed » de la commande [Status](status.md) . Pour spécifier la vitesse plus précisément, utilisez l’indicateur « Speed » de cette commande. Pour videodiscs, « Slow » s’applique uniquement au format CAV.                                                                                                                                                                                            |
| *entier* de vitesse | Lit un videodisc à la vitesse spécifiée, en images par seconde. Cet indicateur s’applique uniquement aux disques CAV.                                                                                                                                                                                                                                                                                                                                                 |
| pour *positionner*   | Spécifie une position de fin pour la lecture. Si l’indicateur « to » n’est pas spécifié, la lecture s’arrête à la fin du contenu. Pour les appareils **cdaudio** , si la position « to » est supérieure à la position de fin du disque, le pilote retourne une erreur. Pour les appareils **videodisc** , les positions par défaut se trouvent dans des frames pour les disques CAV et en heures, minutes et secondes pour les disques CLV.                                                                  |
| window          | Spécifie que la diffusion doit utiliser la fenêtre associée à l’instance d’appareil. Il s'agit du paramètre par défaut.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) . Cette commande commence à la vitesse actuelle, telle qu’elle est définie avec la commande « Speed » définie. La direction est inversée si l’indicateur « Reverse » est spécifié, ou si l’indicateur « to » est spécifié en tant que valeur inférieure à l’indicateur « from ». Si l’indicateur « from » n’est pas spécifié, la lecture commence à la position actuelle. Les indicateurs « to » et « reverse » ne peuvent pas être utilisés ensemble.

## <a name="examples"></a>Exemples

La commande suivante lit l’appareil « mySound » de la position 1000 à la position 2000, en envoyant un message de notification à la fin de la lecture.

``` syntax
play mysound from 1000 to 2000 notify
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

[set](set.md)
</dt> </dl>

 

