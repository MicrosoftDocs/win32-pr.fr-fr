---
title: Message LVM_SETCOLUMNORDERARRAY (commctrl. h)
description: Définit l’ordre de gauche à droite des colonnes dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetColumnOrderArray.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999779"
---
# <a name="lvm_setcolumnorderarray-message"></a>\_Message SETCOLUMNORDERARRAY LVM

Définit l’ordre de gauche à droite des colonnes dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taille, en éléments, de la mémoire tampon au niveau de *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau qui spécifie l’ordre dans lequel les colonnes doivent être affichées, de gauche à droite. Par exemple, si le contenu du tableau est {2,0,1} , le contrôle affiche la colonne 2, la colonne 0 et la colonne 1 dans cet ordre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





