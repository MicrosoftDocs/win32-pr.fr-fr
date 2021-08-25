---
description: Le système diffuse l’événement de l' \_ appareil DBT CONFIGCHANGECANCELED lorsqu’une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: Événement DBT_CONFIGCHANGECANCELED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624144ccd5a87d983d453c8d6a3c0667376c2a1b9340bba83f229a29882bffe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874539"
---
# <a name="dbt_configchangecanceled-event"></a>\_Événement DBT CONFIGCHANGECANCELED

Le système diffuse l’événement de l' \_ appareil DBT CONFIGCHANGECANCELED lorsqu’une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.

Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ CONFIGCHANGECANCELED et *lParam* défini sur zéro.


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

Définissez sur DBT \_ CONFIGCHANGECANCELED.

</dd> <dt>

*lParam* 
</dt> <dd>

Définit la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

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

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> </dl>

 

 




