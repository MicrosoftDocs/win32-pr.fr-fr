---
description: Le système diffuse l' \_ événement de l’appareil DBT DEVICEQUERYREMOVEFAILED lorsqu’une demande de suppression d’un périphérique ou d’un élément multimédia a été annulée.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: Événement DBT_DEVICEQUERYREMOVEFAILED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605c2689d7d986b4e85fda6d8ce5f24fa6483641de46a6a84f3e4e96ba473897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076303"
---
# <a name="dbt_devicequeryremovefailed-event"></a>\_Événement DBT DEVICEQUERYREMOVEFAILED

Le système diffuse l' \_ événement de l’appareil DBT DEVICEQUERYREMOVEFAILED lorsqu’une demande de suppression d’un périphérique ou d’un élément multimédia a été annulée.

Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEQUERYREMOVEFAILED et *lParam* défini comme indiqué ci-dessous.


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

Définissez sur DBT \_ DEVICEQUERYREMOVEFAILED.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure identifiant l’appareil. La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil. Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [traitement d’une demande de suppression d’un appareil](processing-a-request-to-remove-a-device.md).

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

 

 




