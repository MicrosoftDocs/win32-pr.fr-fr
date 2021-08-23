---
title: IMAGELISTSTATEFLAGS (commctrl. h)
description: Les indicateurs suivants sont passés à la méthode IImageList Draw dans le membre fState de IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb4eef2f744c78e84999e9f07f3ca5a06d5dbf93dbfa26d5c6593d94d4e19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576139"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

Les indicateurs suivants sont passés à la méthode [**IImageList ::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) dans le membre **fState** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante/valeur                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**Ils \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>       | L’état de l’image n’est pas modifié.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**Ils \_ ÉCLAT**</dt> <dt>0x00000001</dt> </dl>             | Non pris en charge. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**Ils \_ OMBRE**</dt> <dt></dt> dépendante </dl>       | Non pris en charge. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**Ils \_ SATURATION**</dt> <dt>0x00000004</dt> </dl> | Réduit la saturation de la couleur de l’icône à des nuances de gris. Cela affecte uniquement les images 32bpp. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**Ils \_ ALPHA**</dt> <dt>0x00000008</dt> </dl>          | Alpha fusionne l’icône. La fusion alpha contrôle le niveau de transparence d’une icône, en fonction de la valeur de son canal alpha. La valeur du canal alpha est indiquée par le membre **Frame** dans la méthode [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) . Le canal alpha peut être compris entre 0 et 255, 0 étant complètement transparent, et 255 entièrement opaque.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

