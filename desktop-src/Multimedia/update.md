---
title: commande Update
description: La commande de mise à jour repeint le frame actuel dans le contexte de périphérique (DC) spécifié. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- commande de mise à jour Windows multimédia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229763"
---
# <a name="update-command"></a>commande Update

La commande de mise à jour repeint le frame actuel dans le contexte de périphérique (DC) spécifié. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*
</dt> <dd>

Handle d’un DC. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande de **mise à jour** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                       | Signification         |
|--------------|-------------------------------|-----------------|
| digitalvideo | HDC *HDC* HDC *HDC* au *Rect* | peindre HDC *HDC* |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszHDC** et leurs significations.



| Valeur               | Signification                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| HDC *HDC*           | Spécifie le handle du contrôleur de périphérique à peindre.                                                               |
| HDC *HDC* au *recto* | Spécifie le rectangle de découpage par rapport au rectangle client.                                     |
| peindre HDC *HDC*     | Peint le DC lorsque l’application reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) destiné à un contrôleur de périphérique. |



 

Pour spécifier le descripteur du DC, utilisez la chaîne « HDC » suivie d’une représentation ASCII du descripteur. Le rectangle est spécifié en tant que **x1 Y1 x2 Y2**. Les coordonnées **x1 Y1** spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées **x2 Y2** spécifient la largeur et la hauteur.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="examples"></a>Exemples

La commande suivante met à jour l’intégralité de la fenêtre d’affichage utilisée par l’appareil « Movie ». Le nombre 203 est un handle vers un contrôleur de périphérique obtenu à partir de la fonction [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .

``` syntax
update movie hdc 203
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

 

