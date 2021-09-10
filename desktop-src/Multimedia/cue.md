---
title: CUE, commande
description: La commande de pile se prépare à la diffusion ou à l’enregistrement. Les périphériques numériques vidéo, magnétoscope et Waveform-Audio reconnaissent cette commande.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- commande de pile Windows multimédia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6398d4773b6c92332e8a95996e4d81941a073fe
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363687"
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




| Valeur | Signal | Signal | 
|-------|-----|-----|
| digitalvideo | <ul><li>entrée</li><li>NoShow</li></ul> | <ul><li>sortie</li><li>pour <em>positionner</em></li></ul> | 
| vidéo | <ul><li>à partir de la <em>position</em></li><li>entrée</li><li>sortie</li></ul> | <ul><li>preroll</li><li>reverse</li><li>pour <em>positionner</em></li></ul> | 
| WaveAudio | entrée | sortie | 




 

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

## <a name="remarks"></a>Remarques

Bien qu’il ne soit pas nécessaire, l’émission de la commande de pile avant la création ou l’enregistrement sur certains appareils peut réduire le délai avant que l’appareil ne démarre l’action.

Cette commande échoue si la diffusion ou l’enregistrement est en cours ou si l’appareil est suspendu.

Quand cueing pour la lecture (à l’aide de la « sortie » du signal), l’émission de la commande [Play](play.md) avec l’indicateur « from », « to » ou « reverse » annule la commande CUE.

Quand cueing pour l’enregistrement (à l’aide de la balise « Input »), l’émission de la commande [Record](record.md) avec l’indicateur « from », « to » ou « Initialize » annule la commande CUE.

## <a name="examples"></a>Exemples

La commande suivante prépare l’appareil « mySound » pour l’enregistrement.

``` syntax
cue mysound input
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

[répétition](play.md)
</dt> <dt>

[enregistrement](record.md)
</dt> </dl>

 

