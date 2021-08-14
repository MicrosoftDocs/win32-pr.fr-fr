---
title: Styles de contrôle de pagineur (CommCtrl. h)
description: Cette section répertorie les styles de fenêtre utilisés lors de la création de contrôles de pagineur.
ms.assetid: 619fd8cc-e231-41af-8744-a29d14f2c6f8
topic_type:
- apiref
api_name:
- PGS_AUTOSCROLL
- PGS_DRAGNDROP
- PGS_HORZ
- PGS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b97c7df35fc1883274e42fe54c9ff62415da5dca7e2f020b9371ea873fecc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170216"
---
# <a name="pager-control-styles"></a>Styles de contrôle de pagineur

Cette section répertorie les styles de fenêtre utilisés lors de la création de contrôles de pagineur.



| Constante                                                                                                                                                         | Description                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGS_AUTOSCROLL"></span><span id="pgs_autoscroll"></span><dl> <dt>**DÉFILEMENT automatique PG \_**</dt> </dl> | Le contrôle de pagineur défile lorsque l’utilisateur place la souris sur l’un des boutons de défilement.<br/>                                                                                                                     |
| <span id="PGS_DRAGNDROP"></span><span id="pgs_dragndrop"></span><dl> <dt>**PG \_ DRAGNDROP**</dt> </dl>    | La fenêtre contenue peut être une cible de glisser-déplacer. Le contrôle de pagineur effectue automatiquement un défilement si un élément est déplacé de l’extérieur du pagineur sur l’un des boutons de défilement.<br/>                                     |
| <span id="PGS_HORZ"></span><span id="pgs_horz"></span><dl> <dt>**PG \_ Horiz**</dt> </dl>                   | Crée un contrôle de pagineur qui peut faire défiler horizontalement. Ce style et le style **PG \_ vert** s’excluent mutuellement et ne peuvent pas être combinés.<br/>                                                                 |
| <span id="PGS_VERT"></span><span id="pgs_vert"></span><dl> <dt>**PG \_ vert**</dt> </dl>                   | Crée un contrôle de pagineur qui peut être défilé verticalement. Il s’agit de la direction par défaut si aucun style de direction n’est spécifié. Ce style et le **style \_ Hori PG** s’excluent mutuellement et ne peuvent pas être combinés.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





