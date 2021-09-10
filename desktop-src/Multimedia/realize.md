---
title: commande de réalisation
description: La commande de réalisation indique à un appareil de sélectionner et de réaliser sa palette dans le contexte d’affichage de la fenêtre affichée. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- réalisez Windows commande multimédia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363991"
---
# <a name="realize-command"></a>commande de réalisation

La commande de réalisation indique à un appareil de sélectionner et de réaliser sa palette dans le contexte d’affichage de la fenêtre affichée. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*
</dt> <dd>

Un des indicateurs suivants.



| Valeur      | Signification                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Réalise la palette sous forme de palette d’arrière-plan.                             |
| normal     | Réalise la palette pour une fenêtre de niveau supérieur. Il s'agit du paramètre par défaut. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Utilisez cette commande uniquement si votre application utilise un handle de fenêtre et reçoit un message **WM \_ QUERYNEWPALLETTE** ou **WM \_ PALETTECHANGED** .

## <a name="examples"></a>Exemples

La commande suivante indique à l’appareil « MyVideo » de réaliser sa palette.

``` syntax
realize myvideo normal
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
</dt> </dl>

 

