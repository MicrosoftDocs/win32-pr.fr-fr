---
title: commande put
description: La commande put définit la zone de l’image source et de la fenêtre de destination utilisées pour l’affichage. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- commande put Windows multimédia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105706"
---
# <a name="put-command"></a>commande put

La commande put définit la zone de l’image source et de la fenêtre de destination utilisées pour l’affichage. Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*
</dt> <dd>

Indicateur pour la définition de la zone. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande put et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                                                      | Signification                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | destination de destination *au niveau* du frame du rectangle dans le rectangle *source source au* *rectangle* | vidéo vidéo dans la fenêtre *rectangle* fenêtre fenêtre du *rectangle* client fenêtre client au niveau du *rectangle* |
| superposition      | destination de destination au niveau du frame du *rectangle* dans le *rectangle*                             | vidéo source de la vidéo du *rectangle* dans le *rectangle*                                           |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszRegions** et leurs significations.



| Valeur                        | Signification                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination                  | Sélectionne la zone cliente entière de la fenêtre de destination pour afficher les données.                                                                                                                                                                                                                                                                         |
| destination au niveau du *rectangle*   | Sélectionne une partie de la zone cliente de la fenêtre de destination utilisée pour afficher l’image. Lorsqu’une zone de la fenêtre d’affichage est spécifiée et que l’appareil prend en charge l’étirement, l’image source est étirée jusqu’à l’offset et l’étendue de destination.                                                                                                     |
| frame                        | Sélectionne la mémoire tampon de frame entière pour recevoir les images vidéo entrantes.                                                                                                                                                                                                                                                                                 |
| Frame au niveau du *rectangle*         | Sélectionne une partie de la mémoire tampon de trame pour recevoir les images vidéo entrantes.                                                                                                                                                                                                                                                                           |
| source                       | Sélectionne la totalité de l’image à afficher dans la fenêtre de destination.                                                                                                                                                                                                                                                                                       |
| source au *rectangle*        | Sélectionne une partie de l’image à afficher dans la fenêtre de destination. Lorsqu’une zone de l’image source est spécifiée et que l’appareil prend en charge l’étirement, l’image source est étirée jusqu’au décalage et à l’étendue de destination.                                                                                                                           |
| video                        | Sélectionne la totalité de l’image vidéo entrante à capturer dans la mémoire tampon de trame.                                                                                                                                                                                                                                                                               |
| vidéo au niveau du *rectangle*         | Sélectionne une partie de l’image vidéo entrante à capturer dans la mémoire tampon de trame.                                                                                                                                                                                                                                                                         |
| window                       | Restaure la taille initiale de la fenêtre à l’écran. Cette commande affiche également la fenêtre.                                                                                                                                                                                                                                                               |
| fenêtre au *rectangle*        | Modifie la taille et l’emplacement de la fenêtre d’affichage. Le rectangle spécifié est relatif à la fenêtre parente de la fenêtre d’affichage (généralement le bureau) si l’indicateur « style Child » a été utilisé pour la commande [Open](open.md) . Pour modifier l’emplacement de la fenêtre sans modifier sa hauteur ou sa largeur, spécifiez une valeur égale à zéro pour la hauteur et la largeur. |
| client Windows                | Restaure la zone cliente de la fenêtre.                                                                                                                                                                                                                                                                                                               |
| client Windows au *rectangle* | Modifie la taille et l’emplacement de la zone cliente de la fenêtre. Le rectangle spécifié est relatif à la fenêtre parente de la fenêtre cliente. Pour modifier l’emplacement de la fenêtre sans modifier sa hauteur ou sa largeur, spécifiez une valeur égale à zéro pour la hauteur et la largeur.                                                                                      |



 

Lorsqu’un indicateur comprend un rectangle, les coordonnées des rectangles sont relatives à l’origine de la fenêtre ou à l’origine de l’image, selon le cas, et sont spécifiées comme **x1 Y1 x2 Y2**. Les coordonnées **X1Y1** spécifient l’angle supérieur gauche, tandis que les coordonnées **X2Y2** spécifient la largeur et la hauteur du rectangle.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

La commande put définit un ou plusieurs des rectangles suivants lorsque vous travaillez avec des appareils de superposition vidéo :

-   Le rectangle vidéo définit la région de l’image vidéo entrante à capturer.
-   Le rectangle de cadre définit la région de la mémoire tampon de trame qui reçoit l’image vidéo entrante.
-   Le rectangle source définit la région de la mémoire tampon de trame qui est copiée dans le rectangle de destination.
-   Le rectangle de destination définit la région de la zone cliente de la fenêtre d’affichage qui reçoit l’image vidéo.

Le rectangle vidéo est lié au rectangle de cadre de la même façon que le rectangle source est lié au rectangle de destination. L’étirement peut se produire du rectangle vidéo vers le rectangle de frame et du rectangle source vers le rectangle de destination. Tous les appareils ne prennent pas en charge l’étirement et l’étirement doit être activé (à l’aide de la commande [Set](set.md) ).

La commande suivante définit trois régions pour la vidéo, le frame et la source.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

Les régions de cet exemple sont définies comme suit :

-   Une région de 200 x 200 pixels des données vidéo entrantes, en commençant à l’origine 120 pixels de l’angle supérieur gauche, sera capturée dans la mémoire tampon de trame.
-   Les données vidéo seront placées dans une région de 200 par 200 pixels dans le coin supérieur gauche de la mémoire tampon de trame.
-   Les transferts sont effectués à partir de la région 200-par 200-pixels située dans le coin supérieur gauche de la mémoire tampon de trame vers la fenêtre de destination.

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

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

