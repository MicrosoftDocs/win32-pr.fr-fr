---
title: IMAGELISTDRAWFLAGS (commctrl. h)
description: Passé à la méthode IImageList Draw dans le membre fStyle de IMAGELISTDRAWPARAMS.
ms.assetid: 99fd2cb2-0cb0-40c2-b184-b6d8e54397b4
topic_type:
- apiref
api_name:
- ILD_NORMAL
- ILD_TRANSPARENT
- ILD_BLEND25
- ILD_FOCUS
- ILD_BLEND50
- ILD_SELECTED
- ILD_BLEND
- ILD_MASK
- ILD_IMAGE
- ILD_ROP
- ILD_OVERLAYMASK
- ILD_PRESERVEALPHA
- ILD_SCALE
- ILD_DPISCALE
- ILD_ASYNC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0743fc2778b3ef693646327fe8206ebedcb89e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941953"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Passé à la méthode [**IImageList ::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) dans le membre **fStyle** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante/valeur                                                                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**Icher \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>                      | Dessine l’image à l’aide de la couleur d’arrière-plan de la liste d’images. Si la couleur d’arrière-plan est la \_ valeur CLR None, l’image est dessinée de manière transparente à l’aide du masque.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**Icher \_ TRANSPARENT**</dt> <dt>0x00000001</dt> </dl>       | Dessine l’image de manière transparente à l’aide du masque, quelle que soit la couleur d’arrière-plan. Cette valeur n’a aucun effet si la liste d’images ne contient pas de masque.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**Icher \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Dessine l’image, en fusionnant 25% avec la couleur de fusion spécifiée par **rgbFg**. Cette valeur n’a aucun effet si la liste d’images ne contient pas de masque.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**Icher \_ FOCUS**</dt> <dt>0x00000002</dt> </dl>                         | Identique à **icher \_ BLEND25**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**Icher \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Dessine l’image, en fusionnant 50 pour cent avec la couleur de fusion spécifiée par **rgbFg**. Cette valeur n’a aucun effet si la liste d’images ne contient pas de masque.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**Icher \_**</dt> <dt>0x00000004</dt> sélectionné </dl>                | Identique à **icher \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**Icher \_ BLEND**</dt> <dt>0x00000004</dt> </dl>                         | Identique à **icher \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**Icher \_ Masquer**</dt> <dt>0x00000010</dt> </dl>                            | Dessine le masque.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**Icher \_ IMAGE**</dt> <dt>0x00000020</dt> </dl>                         | Si la superposition ne nécessite pas le dessin d’un masque, définissez cet indicateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**Icher \_**</dt> <dt>0x00000040</dt> ROP </dl>                               | Dessine l’image à l’aide du code d’opération Raster spécifié par le membre **dwRop** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**Icher \_ OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | Pour extraire l’image de superposition du membre **fStyle** , utilisez l’opérateur logique and pour combiner **fStyle** avec la valeur **\_ OVERLAYMASK icher** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**Icher \_ PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | Conserve le canal alpha dans la destination.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**Icher \_**</dt>Mettre à l’échelle <dt>0x00002000</dt> </dl>                         | Entraîne la mise à l’échelle de l’image en CX, CY au lieu d’être découpée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**Icher \_ DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | Met à l’échelle l’image à la résolution actuelle de l’affichage.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**Icher \_**</dt> <dt>0x00008000</dt> asynchrone </dl>                         | **Windows Vista et versions ultérieures.** Dessine l’image si elle est disponible dans le cache. Ne l’extrayez pas automatiquement. La méthode de dessin appelée retourne E \_ en attente au composant appelant, qui doit ensuite prendre une autre action, telle que, fournir une autre image et mettre en file d’attente une tâche en arrière-plan pour forcer le chargement de l’image via [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) à l’aide de l' \_ indicateur ILFIP Always. L' \_ indicateur Async icher empêche ensuite l’opération d’extraction de bloquer le thread actuel et est particulièrement important si une méthode de dessin est appelée à partir du thread d’interface utilisateur (IU).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

