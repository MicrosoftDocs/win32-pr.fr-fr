---
description: Le système diffuse l’événement de l' \_ appareil DBT DEVNODES \_ Changed lorsqu’un appareil a été ajouté ou supprimé du système. Les applications qui maintiennent des listes d’appareils dans le système doivent actualiser leurs listes.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: Événement DBT_DEVNODES_CHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110694"
---
# <a name="dbt_devnodes_changed-event"></a>\_Événement DBT DEVNODES \_ Changed

Le système diffuse l’événement de l' \_ appareil DBT DEVNODES \_ Changed lorsqu’un appareil a été ajouté ou supprimé du système. Les applications qui maintiennent des listes d’appareils dans le système doivent actualiser leurs listes.

Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVNODES \_ Changed et *lParam* défini sur zéro.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
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

Défini sur DBT \_ DEVNODES \_ Changed.

</dd> <dt>

*lParam* 
</dt> <dd>

Définit la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="remarks"></a>Notes

Il n’y a pas d’informations supplémentaires sur l’appareil qui a été ajouté ou supprimé du système. Les applications qui requièrent plus d’informations doivent s’inscrire à la notification de l’appareil à l’aide de la fonction [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .

## <a name="requirements"></a>Configuration requise



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

[**\_HDR de diffusion dev \_**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> </dl>

 

 




