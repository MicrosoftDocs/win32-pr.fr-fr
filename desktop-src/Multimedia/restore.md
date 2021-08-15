---
title: commande Restore
description: La commande Restore copie une image continue d’un fichier vers la mémoire tampon de trame. Il s’agit de l’inverse de la commande de capture. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- commande restore Windows multimédia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e82fdec2480cfe2fc1b41901872aef7e41ee468d1adc3924df17a27e40031e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689189"
---
# <a name="restore-command"></a>commande Restore

La commande Restore copie une image continue d’un fichier vers la mémoire tampon de trame. Il s’agit de l’inverse de la commande de [capture](capture.md) . Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*
</dt> <dd>

Un ou plusieurs des indicateurs suivants.



| Valeur           | Signification                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle*  | Spécifie un rectangle par rapport à l’origine de la mémoire tampon du frame. Le *rectangle* est spécifié en tant que *x1 Y1 x2 Y2*. Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche et les coordonnées *x2 Y2* spécifient la largeur et la hauteur. Si cet indicateur n’est pas utilisé, l’image est copiée dans l’angle supérieur gauche de la mémoire tampon de trame.<br/> |
| à partir du *nom de fichier* | Spécifie le nom du fichier image à rappeler. Cet indicateur est obligatoire.                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les appareils peuvent reconnaître un large éventail de formats d’image. une image bitmap indépendante du périphérique Windows est toujours reconnue.

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

[attire](capture.md)
</dt> </dl>

 

