---
title: Save, commande
description: La commande Save enregistre un fichier MCI. Les périphériques vidéo-superposition et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne le prennent pas en charge.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- enregistrer la commande Windows multimédia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363919"
---
# <a name="save-command"></a>Save, commande

La commande Save enregistre un fichier MCI. Les périphériques vidéo-superposition et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne le prennent pas en charge.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

Indicateur spécifiant le nom du fichier en cours d’enregistrement et, éventuellement, les indicateurs supplémentaires qui modifient l’opération d’enregistrement. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Save** et les indicateurs utilisés par chaque type.



| Valeur        | Signification              | Signification               |
|--------------|----------------------|-----------------------|
| digitalvideo | abandonner au niveau du *rectangle* | *nom de fichier* keepreserve |
| superposition      | au niveau du *rectangle*       | *extension*            |
| sequencer    | *extension*           |                       |
| WaveAudio    | *extension*           |                       |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszFilename** et leurs significations.



| Valeur          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Arrête une opération d' **enregistrement** en cours. S’il est utilisé, il doit s’agir du seul élément présent.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| au niveau du *rectangle* | Spécifie un rectangle par rapport à l’origine de la mémoire tampon du frame. Le *rectangle* est spécifié en tant que *x1 Y1 x2 Y2*. Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche et les coordonnées *x2 Y2* spécifient la largeur et la hauteur. Pour les périphériques vidéo numériques, la commande de [capture](capture.md) est utilisée pour capturer le contenu de la mémoire tampon de trame.<br/>                                                                                                                                               |
| *extension*     | Spécifie le nom de fichier à assigner au fichier de données. Si aucun chemin d’accès n’est spécifié, le fichier est placé sur le disque et dans le répertoire spécifié précédemment dans la commande de [réserve](reserve.md) explicite ou implicite. Si la **réserve** n’a pas été émise, le lecteur et le répertoire par défaut sont ceux associés à la tâche de l’application. Si un chemin d’accès est spécifié, l’appareil peut exiger qu’il se trouve sur le lecteur de disque spécifié par la **réserve** explicite ou implicite. Cet indicateur est obligatoire. |
| keepreserve    | Spécifie que l’espace disque inutilisé à partir de la commande de **réserve** d’origine n’est pas libéré.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

La variable *filename* est requise si l’appareil a été ouvert à l’aide de l’identificateur de périphérique « New ».

## <a name="examples"></a>Exemples

La commande suivante enregistre l’intégralité de la mémoire tampon vidéo dans un fichier nommé VCAPFILE. TGA.

``` syntax
save vboard c:\vcap\vcapfile.tga
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

[attire](capture.md)
</dt> <dt>

[reserve](reserve.md)
</dt> </dl>

 

