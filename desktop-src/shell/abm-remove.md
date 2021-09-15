---
description: Annule l’inscription d’un appbar en le supprimant de la liste interne du système. Le système n’envoie plus de messages de notification à appbar ou empêche d’autres applications d’utiliser la zone d’écran utilisée par le appbar.
title: Message ABM_REMOVE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296138"
---
# <a name="abm_remove-message"></a>ABM \_ supprimer le message

Annule l’inscription d’un appbar en le supprimant de la liste interne du système. Le système n’envoie plus de messages de notification à appbar ou empêche d’autres applications d’utiliser la zone d’écran utilisée par le appbar.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pabd* 
</dt> <dd>

Pointeur vers une structure [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) qui contient le handle du appbar dont l’inscription doit être annulée. Vous devez spécifier les membres **cbSize** et **HWND** lors de l’envoi de ce message. tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne toujours la **valeur true**.

## <a name="remarks"></a>Notes

Ce message amène le système à envoyer le message de notification [**ABN \_ POSCHANGED**](abn-poschanged.md) à tous les barres.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




