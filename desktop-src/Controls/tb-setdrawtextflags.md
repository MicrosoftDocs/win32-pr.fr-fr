---
title: Message TB_SETDRAWTEXTFLAGS (commctrl. h)
description: Définit les indicateurs de dessin de texte pour la barre d’outils.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849bbb0e661c9e8afe246894d2d2f59d99d15a3f096ad2295a7018cf3df26ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543879"
---
# <a name="tb_setdrawtextflags-message"></a>TO \_ SETDRAWTEXTFLAGS message

Définit les indicateurs de dessin de texte pour la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Un ou plusieurs des indicateurs DT \_ , spécifiés dans [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), qui indiquent les bits de *lParam* qui seront utilisés lors du dessin du texte.

</dd> <dt>

*lParam* 
</dt> <dd>

Un ou plusieurs des indicateurs DT \_ , spécifiés dans [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext), qui indiquent comment le texte du bouton sera dessiné. Cette valeur est transmise à la fonction **DrawText** lorsque le texte du bouton est dessiné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne les indicateurs de dessin de texte précédents.

## <a name="remarks"></a>Remarques

Le paramètre *wParam* vous permet de spécifier les indicateurs qui seront utilisés lors du dessin du texte, même si ces indicateurs sont désactivés. Par exemple, si vous ne souhaitez pas que l' \_ indicateur DT Center soit utilisé lors du dessin de texte, vous devez ajouter l' \_ indicateur DT Center à *wParam* et ne pas spécifier l' \_ indicateur DT Center dans *lParam*. Cela empêche le contrôle de passer l' \_ indicateur DT Center à la fonction [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

