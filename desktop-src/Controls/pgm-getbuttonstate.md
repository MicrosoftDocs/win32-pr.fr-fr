---
title: Message PGM_GETBUTTONSTATE (commctrl. h)
description: Récupère l’état du bouton spécifié dans un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetButtonState.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2014b6e36a0ab883155d786760ef54f02c89ee0d17192d6082d40ad19eec95a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830190"
---
# <a name="pgm_getbuttonstate-message"></a>\_Message GETBUTTONSTATE PGM

Récupère l’état du bouton spécifié dans un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Indique le bouton pour lequel l’État doit être récupéré. Il peut s’agir de l’une des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | Indique le bouton supérieur dans un contrôle de pagineur [**PG \_ vert**](pager-control-styles.md) ou le bouton gauche dans un contrôle de pagineur [**\_ Hori PG**](pager-control-styles.md) . <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | Indique le bouton inférieur dans un contrôle de pagineur [**PG \_ vert**](pager-control-styles.md) ou le bouton droit dans un contrôle de pagineur [**\_ Hori PG**](pager-control-styles.md) . <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’état du bouton spécifié dans *lParam*. Il s’agit d’une ou plusieurs des valeurs suivantes (si plus une valeur est retournée, elles sont combinées à l’aide d’une opération or au niveau du bit) :



| Code de retour                                                                                   | Description                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ invisible**</dt> </dl> | Le bouton n’est pas visible. <br/>      |
| <dl> <dt>**PGF \_ normal**</dt> </dl>    | Le bouton est dans un état normal. <br/>  |
| <dl> <dt>**PGF \_ grisé**</dt> </dl>    | Le bouton est grisé. <br/>  |
| <dl> <dt>**PGF \_ enfoncé**</dt> </dl> | Le bouton est à l’état enfoncé. <br/> |
| <dl> <dt>**PGF \_ chaud**</dt> </dl>       | Le bouton est à l’état actif. <br/>     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





