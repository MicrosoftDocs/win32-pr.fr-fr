---
title: Indicateurs de stylet
description: Valeurs qui peuvent apparaître dans le champ penFlags de la structure POINTER_PEN_INFO.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466130"
---
# <a name="pen-flags"></a>Indicateurs de stylet

Valeurs qui peuvent apparaître dans le champ **penFlags** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Il n’y a pas d’indicateur de stylet. Il s’agit de la valeur par défaut.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Le bouton en barillet est enfoncé.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Le stylet est inversé.


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Le bouton gomme est enfoncé.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





