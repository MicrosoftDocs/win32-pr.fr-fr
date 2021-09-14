---
title: Message TB_SETHOTITEM2 (commctrl. h)
description: 'TB_SETHOTITEM2 message : définit l’élément réactif dans une barre d’outils.'
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116561"
---
# <a name="tb_sethotitem2-message"></a>TO \_ SETHOTITEM2 message

Définit l’élément réactif dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément qui sera rendu chaud. Si cette valeur est-1, aucun des éléments n’est chaud.

</dd> <dt>

*lParam* 
</dt> <dd>Combinaison d’indicateurs HICF \_ xxx. Consultez <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’élément réactif précédent, ou-1 s’il n’y a pas d’élément réactif.

## <a name="remarks"></a>Notes

Le comportement de ce message n’est pas défini pour les barres d’outils qui n’ont pas le style [**\_ plat TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





