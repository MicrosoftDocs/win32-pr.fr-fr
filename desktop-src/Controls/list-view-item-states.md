---
title: List-View les États de l’élément (CommCtrl. h)
description: La valeur d’état d’un élément se compose de l’état de l’élément, d’un index de masque de recouvrement facultatif et d’un index de masque d’image d’État facultatif.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525468"
---
# <a name="list-view-item-states"></a>États de l’élément List-View

La valeur d’état d’un élément se compose de l’état de l’élément, d’un index de masque de recouvrement facultatif et d’un index de masque d’image d’État facultatif.

L’état d’un élément détermine son apparence et ses fonctionnalités. L’État peut être zéro ou une ou plusieurs des valeurs suivantes :



| Constante                                                                                                                                                                        | Description                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**activation de LVIS \_**</dt> </dl>             | Actuellement non pris en charge.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ couper**</dt> </dl>                                  | L’élément est marqué pour une opération couper-coller.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | L’élément est mis en surbrillance en tant que cible de glisser-déplacer.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ concentré**</dt> </dl>                      | L’élément a le focus, donc il est entouré d’un rectangle de focus standard. Bien qu’un seul élément puisse être sélectionné, un seul élément peut avoir le focus.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | L’index d’image de superposition de l’élément est récupéré par un masque.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ sélectionné**</dt> </dl>                   | L'élément est sélectionné. L’apparence d’un élément sélectionné varie selon qu’il a le focus et également sur les couleurs système utilisées pour la sélection.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | L’index d’images d’état de l’élément est récupéré par un masque.<br/>                                                                                                      |



## <a name="remarks"></a>Notes

Vous pouvez utiliser le masque **Lvis \_ OVERLAYMASK** pour isoler l’index de base un de l’image de superposition. Vous pouvez utiliser le masque **Lvis \_ STATEIMAGEMASK** pour isoler l’index de base un de l’image d’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





