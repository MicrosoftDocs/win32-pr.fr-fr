---
title: Message TB_GETINSERTMARKCOLOR (commctrl. h)
description: Récupère la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- TB_GETINSERTMARKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ceebd5f3989ed870cf70ccad819300d85c05d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116754"
---
# <a name="tb_getinsertmarkcolor-message"></a>TO \_ GETINSERTMARKCOLOR message

Récupère la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la couleur de la marque d’insertion actuelle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)
</dt> </dl>

 

