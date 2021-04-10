---
title: Message CB_GETTOPINDEX (winuser. h)
description: Une application envoie le \_ message CB GETTOPINDEX pour récupérer l’index de base zéro du premier élément visible dans la partie zone de liste d’une zone de liste déroulante.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942112"
---
# <a name="cb_gettopindex-message"></a>\_Message GETTOPINDEX CB

Une application envoie le message **CB \_ GETTOPINDEX** pour récupérer l’index de base zéro du premier élément visible dans la partie zone de liste d’une zone de liste déroulante. Initialement, l’élément avec l’index 0 est en haut de la zone de liste, mais si le contenu de la zone de liste a fait l’objet d’un défilement, un autre élément peut se trouver en haut.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est réussi, la valeur de retour est l’index du premier élément visible dans la zone de liste de la zone de liste déroulante.

Si le message échoue, la valeur de retour est CB \_ Err.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTOPINDEX CB**](cb-settopindex.md)
</dt> </dl>

 

 





