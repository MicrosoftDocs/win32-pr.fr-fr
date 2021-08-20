---
title: Message TB_SETMAXTEXTROWS (commctrl. h)
description: Définit le nombre maximal de lignes de texte affichées sur un bouton de barre d’outils.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a1e1a2cda7b3dced4cf538623578d48b41d38925629f2985a35974baed229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167479"
---
# <a name="tb_setmaxtextrows-message"></a>TO \_ SETMAXTEXTROWS message

Définit le nombre maximal de lignes de texte affichées sur un bouton de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre maximal de lignes de texte qui peuvent être affichées.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Pour que le texte soit renvoyé à la ligne, vous devez définir la largeur de bouton maximale en envoyant un message [**\_ SETBUTTONWIDTH to**](tb-setbuttonwidth.md) . Le texte est renvoyé à la ligne au niveau d’un saut de mot ; les sauts de ligne (« \\ n ») dans le texte sont ignorés. Le texte dans les \_ barres d’outils de liste TBSTYLE est toujours affiché sur une seule ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





