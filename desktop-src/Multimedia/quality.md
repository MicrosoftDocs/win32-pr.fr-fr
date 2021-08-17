---
title: Quality (commande)
description: La commande Quality définit un niveau de qualité personnalisé pour la compression des données audio, vidéo ou d’images fixes. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- commande quality Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50f019b0e89f21d792f75c13e6c8e755486009d38d242878fec3121333fb9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372324"
---
# <a name="quality-command"></a>Quality (commande)

La commande Quality définit un niveau de qualité personnalisé pour la compression des données audio, vidéo ou d’images fixes. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

Un ou plusieurs des indicateurs suivants. (L’un des trois indicateurs « audio », « toujours » et « vidéo » doit être présent.)



| Valeur                 | Signification                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algorithme* d’algorithme | Associe le niveau de qualité à l' *algorithme* spécifié. Cet *algorithme* doit être pris en charge par l’appareil et être compatible avec l’indicateur « audio », « toujours » ou « vidéo » utilisé. En cas d’omission, l’algorithme actuel est utilisé. |
| *nom* audio          | Indique que cette commande spécifie un niveau de qualité « audio » identifié par le *nom*.                                                                                                                                                   |
| dialogue                | Demande que l’appareil affiche une boîte de dialogue. Cette boîte de dialogue contient des champs spécifiques à l’algorithme qui sont utilisés en interne par l’appareil pour créer la structure décrivant un niveau de qualité spécifique.                                    |
| handle *de handle*       | Spécifie un *handle* vers une structure qui contient des données algorithmiques qui décrivent un niveau de qualité spécifique. Les structures des données référencées par ce handle sont spécifiques à l’appareil.                                         |
| *nom* toujours          | Indique que la commande spécifie un niveau de qualité « toujours » identifié par le *nom.*                                                                                                                                                     |
| *nom* de la vidéo          | Indique que la commande spécifie un niveau de qualité « vidéo » identifié par le *nom*.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Cette commande définit un nom de chaîne pour le niveau de qualité, qui peut ensuite être utilisé dans une commande [setvideo](setvideo.md) "Quality", setvideo "Still Quality" ou [SetAudio](setaudio.md) "Quality" pour l’établir comme le niveau de qualité de la vidéo, du reste ou de la compression audio en cours.

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

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

