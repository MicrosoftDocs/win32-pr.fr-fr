---
title: Message ICM_DRAW (VFW. h)
description: le ICM \_ message de dessin avertit un pilote de rendu de décompresser un frame de données et de le dessiner à l’écran.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- message ICM_DRAW Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44216e523da62e0dde22abed8d88b9b8aacd8f68119a88f3177f45ecd910029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784989"
---
# <a name="icm_draw-message"></a>ICM \_ DESSINER un message

le **ICM \_** message de dessin avertit un pilote de rendu de décompresser un frame de données et de le dessiner à l’écran.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Pointeur vers une structure [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Si l' \_ indicateur de mise à jour ICDRAW est défini dans le membre **DwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), la zone de l’écran utilisée pour le dessin n’est pas valide et doit être mise à jour. L’étendue de la mise à jour dépend du contenu du membre **lpData** .

Si **lpData** a la **valeur null**, le pilote doit mettre à jour l’intégralité du rectangle de destination avec l’image actuelle. Si le pilote conserve une copie de l’image dans une mémoire tampon hors écran, ce message peut échouer. Si **lpData** n’a pas la **valeur null**, le pilote doit dessiner les données et vérifier que l’intégralité de la destination est mise à jour.

Si l' \_ indicateur ICDRAW HURRYUP est défini dans **dwFlags**, l’application appelante souhaite que le pilote se poursuive le plus rapidement possible, sans doute même mettre à jour l’écran.

Si l' \_ indicateur de PRÉROLL ICDRAW est défini dans **dwFlags**, cette image vidéo est des informations préliminaires et ne doit pas être affichée si possible. Par exemple, si la lecture doit commencer à partir de l’image 10, et que le frame 0 est l’image clé précédente la plus proche, les trames de 0 à 9 comportent le \_ PRÉROLL ICDRAW Set.

si vous souhaitez que le pilote décompresse les données dans une mémoire tampon, envoyez le message [**ICM \_ décompresser**](icm-decompress.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





