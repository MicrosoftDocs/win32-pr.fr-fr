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
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032695"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

