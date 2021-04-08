---
title: CUE, commande
description: La commande de pile se prépare à la diffusion ou à l’enregistrement. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- commande de pile Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844410"
---
# <a name="cue-command"></a>CUE, commande

La commande de pile se prépare à la diffusion ou à l’enregistrement. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Indicateur qui prépare un appareil pour la diffusion ou l’enregistrement. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **CUE** et les indicateurs utilisés par chaque type.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signal</th>
<th>Signal</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>entrée</li>
<li>NoShow</li>
</ul></td>
<td><ul>
<li>sortie</li>
<li>pour <em>positionner</em></li>
</ul></td>
</tr>
<tr class="even">
<td>vidéo</td>
<td><ul>
<li>à partir de la <em>position</em></li>
<li>entrée</li>
<li>sortie</li>
</ul></td>
<td><ul>
<li>preroll</li>
<li>reverse</li>
<li>pour <em>positionner</em></li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td>entrée</td>
<td>sortie</td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszInOutTo* et leurs significations.



| Valeur           | Signification                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| à partir de la *position* | Indique où commencer.                                                                                                                                                                                                                                                                                      |
| entrée           | Prépare l’enregistrement. Pour les périphériques vidéo numériques, cet indicateur peut être omis si la source de présentation actuelle est déjà l’entrée externe.                                                                                                                                                                  |
| NoShow          | Prépare la diffusion d’une image sans l’afficher. Lorsque cet indicateur est spécifié, l’affichage continue d’afficher l’image dans la mémoire tampon de trame, même si son frame correspondant n’est pas la position actuelle. Une commande de pile suivante sans cet indicateur et sans l’indicateur « to » affiche le frame actuel. |
| sortie          | Prépare la durée de la diffusion. Si ni « Input » ni « output » n’est spécifié, le paramètre par défaut est « output ».                                                                                                                                                                                                           |
| preroll         | Déplace la distance du préroll à partir du *point d'* interrogation. L’objet in-point est la position actuelle ou la position spécifiée par l’indicateur « from ».                                                                                                                                                                            |
| reverse         | Indique que la direction de lecture est en sens inverse (arrière).                                                                                                                                                                                                                                                             |
| pour *positionner*   | Déplace l’espace de travail à la position spécifiée. Pour les périphériques VCR, cet indicateur indique l’endroit où s’arrêter.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Bien qu’il ne soit pas nécessaire, l’émission de la commande de pile avant la création ou l’enregistrement sur certains appareils peut réduire le délai avant que l’appareil ne démarre l’action.

Cette commande échoue si la diffusion ou l’enregistrement est en cours ou si l’appareil est suspendu.

Quand cueing pour la lecture (à l’aide de la « sortie » du signal), l’émission de la commande [Play](play.md) avec l’indicateur « from », « to » ou « reverse » annule la commande CUE.

Quand cueing pour l’enregistrement (à l’aide de la balise « Input »), l’émission de la commande [Record](record.md) avec l’indicateur « from », « to » ou « Initialize » annule la commande CUE.

## <a name="examples"></a>Exemples

La commande suivante prépare l’appareil « mySound » pour l’enregistrement.

``` syntax
cue mysound input
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

[répétition](play.md)
</dt> <dt>

[enregistrement](record.md)
</dt> </dl>

 

