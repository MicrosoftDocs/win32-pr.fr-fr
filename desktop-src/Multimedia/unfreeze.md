---
title: libérer la commande
description: La commande dégeler réactive l’acquisition vidéo dans la mémoire tampon de trame une fois qu’elle a été désactivée par la commande Freeze. Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- libérer la commande Windows multimédia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229769"
---
# <a name="unfreeze-command"></a>libérer la commande

La commande dégeler réactive l’acquisition vidéo dans la mémoire tampon de trame une fois qu’elle a été désactivée par la commande [Freeze](freeze.md) . Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

Indicateur pour la réactivation de l’acquisition vidéo dans la mémoire tampon de trame. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **dégeler** et les indicateurs utilisés par chaque type.



| Valeur        | Signification        |
|--------------|----------------|
| digitalvideo | au niveau du *rectangle* |
| superposition      | au niveau du *rectangle* |
| vidéo          | sortie d’entrée   |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszUnfreeze** et leurs significations.



| Valeur          | Signification                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle* | Spécifie la région pour laquelle l’acquisition de vidéos sera réactivée. Le rectangle est relatif à l’origine de la mémoire tampon vidéo et est spécifié comme *x1 Y1 x2 Y2*. Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2 Y2* spécifient la largeur et la hauteur. |
| entrée          | Libérez l’image d’entrée.                                                                                                                                                                                                                                                                  |
| sortie         | Libérez l’image de sortie. Si aucune « entrée » ni « sortie » n’est indiquée, la « sortie » est supposée.                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="examples"></a>Exemples

La commande suivante libère une région de la mémoire tampon vidéo.

``` syntax
unfreeze vboard at 10 20 90 165
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

[antigel](freeze.md)
</dt> </dl>

 

