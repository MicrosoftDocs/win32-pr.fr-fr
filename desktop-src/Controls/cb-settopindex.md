---
title: Message CB_SETTOPINDEX (winuser. h)
description: Une application envoie le \_ message CB SETTOPINDEX pour s’assurer qu’un élément particulier est visible dans la zone de liste d’une zone de liste déroulante.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740117"
---
# <a name="cb_settopindex-message"></a>\_Message SETTOPINDEX CB

Une application envoie le message **CB \_ SETTOPINDEX** pour s’assurer qu’un élément particulier est visible dans la zone de liste d’une zone de liste déroulante. Le système fait défiler le contenu de la zone de liste afin que l’élément spécifié apparaisse en haut de la zone de liste ou que la plage de défilement maximale ait été atteinte.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro de l’élément de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message réussit, la valeur de retour est zéro.

Si le message échoue, la valeur de retour est CB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTOPINDEX CB**](cb-gettopindex.md)
</dt> </dl>

 

 





