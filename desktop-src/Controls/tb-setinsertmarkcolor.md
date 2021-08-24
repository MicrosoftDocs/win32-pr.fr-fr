---
title: Message TB_SETINSERTMARKCOLOR (commctrl. h)
description: Définit la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 466c9bfe27462b11cc0c6cf3a183328ddedb1b422b4d0c07b4496c7a90f83890
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540039"
---
# <a name="tb_setinsertmarkcolor-message"></a>TO \_ SETINSERTMARKCOLOR message

Définit la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **COLORREF** qui contient la nouvelle couleur de la marque d’insertion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **COLORREF** qui contient la couleur de la marque d’insertion précédente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





