---
title: Message CB_GETMINVISIBLE (commctrl. h)
description: Obtient le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- CB_GETMINVISIBLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124138"
---
# <a name="cb_getminvisible-message"></a>\_Message GETMINVISIBLE CB

Obtient le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.

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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est le nombre minimal d’éléments visibles.

## <a name="remarks"></a>Notes

Lorsque le nombre d’éléments dans la liste déroulante est supérieur au minimum, la zone de liste déroulante utilise une barre de défilement.

Ce message est ignoré si le contrôle de zone de liste déroulante a un [**\_ NOINTEGRALHEIGHT SCC**](combo-box-styles.md)de style.

Pour utiliser **CB \_ GETMINVISIBLE**, l’application doit spécifier comctl32.dll version 6 dans le manifeste. Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETMINVISIBLE CB**](cb-setminvisible.md)
</dt> <dt>

[**\_GetMinVisible ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





