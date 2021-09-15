---
title: commande Load
description: La commande Load charge un fichier dans un format spécifique à l’appareil. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- commande de chargement Windows multimédia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413891"
---
# <a name="load-command"></a>commande Load

La commande Load charge un fichier dans un format spécifique à l’appareil. Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*
</dt> <dd>

Chemin d’accès et nom de fichier à charger. Pour les périphériques de superposition vidéo, cela peut également inclure un rectangle cible pour les données. Pour spécifier un rectangle cible, spécifiez « at » suivi de **x1 Y1 x2 Y2**, où **x1 Y1** spécifient l’angle supérieur gauche du rectangle, et **x2 Y2** spécifient la largeur et la hauteur. Le rectangle est relatif à l’origine de la mémoire tampon vidéo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

L’appareil « vidboard » envoie un message de notification lorsque le chargement est terminé.

## <a name="examples"></a>Exemples

La commande suivante charge un fichier dans le périphérique « vidboard ».

``` syntax
load vidboard c:\vid\fish.vid notify
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

 

