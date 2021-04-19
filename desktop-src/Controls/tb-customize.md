---
title: Message TB_CUSTOMIZE (commctrl. h)
description: Affiche la boîte de dialogue Personnaliser la barre d’outils.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509758"
---
# <a name="tb_customize-message"></a>TO \_ personnaliser le message

Affiche la boîte de dialogue **personnaliser la barre d’outils** .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

> [!Note]  
> La barre d’outils doit gérer les notifications [TBN \_ QUERYINSERT](tbn-queryinsert.md) et [TBN \_ QUERYDELETE](tbn-querydelete.md) pour que la boîte de dialogue **personnaliser la barre d’outils** s’affiche. Si la barre d’outils ne gère pas ces notifications, la **\_ personnalisation to** n’a aucun effet.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





