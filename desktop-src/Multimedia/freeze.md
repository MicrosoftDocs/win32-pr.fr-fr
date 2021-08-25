---
title: figer, commande
description: La commande Freeze fige l’entrée vidéo ou la sortie vidéo sur un magnétoscope ou désactive l’acquisition vidéo dans la mémoire tampon de trame. Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- figer la commande Windows multimédia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1261cc75575a5b59d200ff965a5325caef9fa966
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481555"
---
# <a name="freeze-command"></a>figer, commande

La commande Freeze fige l’entrée vidéo ou la sortie vidéo sur un magnétoscope ou désactive l’acquisition vidéo dans la mémoire tampon de trame. Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

Indicateur qui identifie les éléments à figer. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Freeze** et les indicateurs utilisés par chaque type.




| Valeur | Signification | Signification | 
|-------|---------|---------|
| digitalvideo | au niveau du <em>rectangle</em> | extérieurs | 
| superposition | au niveau du <em>rectangle</em> | 
| vidéo | <ul><li>field</li><li>frame</li></ul> | <ul><li>entrée</li><li>sortie</li></ul> | 




 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszFreezeFlags* et leurs significations.



| Valeur          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle* | Spécifie la région qui sera figée. Pour les périphériques de superposition vidéo, l’acquisition de vidéos est désactivée pour cette région. Pour les périphériques vidéo numériques, le bit du masque de verrouillage est activé sur les pixels du rectangle (sauf si l’indicateur « extérieur » est spécifié). Le rectangle est relatif à l’origine de la mémoire tampon vidéo et est spécifié comme *x1 Y1 x2 Y2*. Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2 Y2* spécifient la largeur et la hauteur. |
| field          | Fige le premier champ. Le champ est supposé par défaut (si ni le cadre ni le champ n’est spécifié).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Fige le frame entier, en affichant les deux champs.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| entrée          | Fige le frame actuel de l’image d’entrée, qu’elle soit en pause ou en cours d’exécution.                                                                                                                                                                                                                                                                                                                                                                                                                |
| sortie         | Fige le frame actuel de la sortie à partir du magnétoscope. Si le magnétoscope est en cours d’exécution lorsque le blocage est émis, le frame actuel est figé et le magnétoscope est suspendu. Si le magnétoscope est suspendu lorsque cette commande est émise, le frame actuel est figé. L’image figée reste sur le périphérique de sortie jusqu’à ce qu’une commande de [décongélation](unfreeze.md) soit émise. Si ni « Input » ni « output » n’est spécifié, « output » est supposé.                                                                                    |
| extérieurs        | Indique que la zone en dehors de la région spécifiée à l’aide de l’indicateur « at » est figée.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Utilisée avec les périphériques VCR, cette commande est destinée aux cartes de saisie de trame.

Pour spécifier des régions d’acquisition irrégulière avec l’indicateur « at », utilisez une série de [commandes Freeze et dégeler.](unfreeze.md) Certains périphériques de superposition vidéo limitent la complexité de la région d’acquisition.

Cette commande est prise en charge uniquement si un appel à la commande [Capability](capability.md) avec l’indicateur « peut se figer » retourne la **valeur true**.

## <a name="examples"></a>Exemples

La commande suivante désactive l’acquisition vidéo dans un carré de 100 pixels dans le coin supérieur gauche de la mémoire tampon vidéo.

``` syntax
freeze vboard at 0 0 100 100
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

[capability](capability.md)
</dt> <dt>

[libérer](unfreeze.md)
</dt> </dl>

 

