---
title: commande Where
description: La commande WHERE récupère le rectangle spécifiant la zone source ou de destination. Ce rectangle a été spécifié à l’aide de la commande put. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- commande Windows multimédia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942686"
---
# <a name="where-command"></a>commande Where

La commande WHERE récupère le rectangle spécifiant la zone source ou de destination. Ce rectangle a été spécifié à l’aide de la commande [put](put.md) . Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*
</dt> <dd>

Indicateur qui identifie le rectangle dont les dimensions sont récupérées. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Where** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                       | Signification                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| digitalvideo | destinationdestination [**Max**](max.md)frameFrame maxsource | maxvideovideo source maxwindowwindow Max |
| superposition      | destinationframe                                              | sourcevideo                              |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRequestRect** et leurs significations.



| Valeur                          | Signification                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                    | Récupère l’étendue et le décalage de destination. Pour les périphériques de superposition vidéo, le rectangle de destination définit la zone de la zone cliente de la fenêtre d’affichage qui affiche les données de l’image à partir de la mémoire tampon de trame.                                                                                             |
| maximum de la destination [ ](max.md) | Récupère la taille actuelle du rectangle client.                                                                                                                                                                                                                                                  |
| frame                          | Récupère le décalage et l’étendue du rectangle de la mémoire tampon de frame. Le rectangle de la mémoire tampon de frame définit la zone de la mémoire tampon de trame qui reçoit les données vidéo entrantes. Les images du rectangle « Video » sont mises à l’échelle dans cette région.                                                                     |
| [ **nombre maximal** de frames](max.md)       | Retourne la taille maximale de la mémoire tampon de trame.                                                                                                                                                                                                                                                        |
| source                         | Récupère l’étendue et le décalage de la source. Pour les périphériques de superposition vidéo, le rectangle source définit la région de la mémoire tampon de trame qui s’affiche dans la fenêtre de destination. L’appareil utilise ce rectangle pour rogner l’image avant qu’elle ne soit étirée pour s’ajuster au rectangle de destination sur l’affichage. |
| [ **Max** source](max.md)      | Récupère la taille maximale de la mémoire tampon de trame.                                                                                                                                                                                                                                                      |
| video                          | Récupère le décalage et l’étendue du rectangle vidéo. Le rectangle vidéo définit la région des données vidéo entrantes qui sont transférées vers la mémoire tampon de trame.                                                                                                                                   |
| [ **Max** . vidéo](max.md)       | Retourne la taille maximale de l’entrée.                                                                                                                                                                                                                                                               |
| window                         | Récupère la taille et la position actuelles du frame de fenêtre d’affichage.                                                                                                                                                                                                                                 |
| maximum de la fenêtre [ ](max.md)      | Récupère la taille de l’affichage entier.                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un rectangle dans le paramètre *lpszReturnString* de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Le rectangle décrit la zone spécifiée dans le paramètre *lpszRequestRect* de cette commande. Le rectangle est spécifié en tant que *x1 Y1 x2 Y2*. Les coordonnées *x1 Y1* spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées *x2 Y2* spécifient la largeur et la hauteur.

## <a name="examples"></a>Exemples

La commande suivante renvoie le rectangle d’affichage de l’appareil « Movie ».

``` syntax
where movie destination
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

[posé](put.md)
</dt> </dl>

 

