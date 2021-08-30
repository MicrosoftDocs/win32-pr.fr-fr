---
title: Message RB_SHOWBAND (commctrl. h)
description: Affiche ou masque une bande donnée dans un contrôle rebar.
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- RB_SHOWBAND les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312344248dbf280e1f46d52efd7b4960b47625131d29d30c410939c19b593e5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985379"
---
# <a name="rb_showband-message"></a>\_Message SHOWBAND RB

Affiche ou masque une bande donnée dans un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro d’une bande dans le contrôle rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **booléenne** qui indique si la bande doit être affichée ou masquée. Si cette valeur est différente de zéro, la bande est affichée. Dans le cas contraire, la bande sera masquée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





