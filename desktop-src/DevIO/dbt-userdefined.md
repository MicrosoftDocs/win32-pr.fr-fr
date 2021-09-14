---
description: L' \_ événement d’appareil DBT USERDEFINED identifie un événement défini par l’utilisateur.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Événement DBT_USERDEFINED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114393"
---
# <a name="dbt_userdefined-event"></a>\_Événement USERDEFINED DBT

L' \_ événement d’appareil DBT USERDEFINED identifie un événement défini par l’utilisateur.

Pour diffuser cet événement d’appareil, appelez la fonction [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) avec le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) . Affectez à *wParam* la valeur DBT \_ USERDEFINED et définissez *lParam* comme indiqué ci-dessous.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle d'une fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificateur du message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Défini sur DBT \_ USERDEFINED.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**\_ \_ \_ USERDEFINED de diffusion de développement**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) qui décrit la diffusion définie par l’utilisateur en cours. Le membre **dbud \_ szName** contient le nom du message défini par l’utilisateur, suivi de toutes les données définies par l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de l’appareil](device-events.md)
</dt> <dt>

[Événements de gestion des appareils](device-management-events.md)
</dt> <dt>

[**\_\_USERDEFINED de diffusion dev \_**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

