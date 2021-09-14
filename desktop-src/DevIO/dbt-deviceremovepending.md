---
description: Le système diffuse l' \_ événement de l’appareil DBT DEVICEREMOVEPENDING lorsqu’un périphérique ou un élément multimédia est en cours de suppression et n’est plus disponible.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: Événement DBT_DEVICEREMOVEPENDING (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114402"
---
# <a name="dbt_deviceremovepending-event"></a>\_Événement DBT DEVICEREMOVEPENDING

Le système diffuse l' \_ événement de l’appareil DBT DEVICEREMOVEPENDING lorsqu’un périphérique ou un élément multimédia est en cours de suppression et n’est plus disponible.

Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEREMOVEPENDING et *lParam* défini comme indiqué ci-dessous.


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

Définissez sur DBT \_ DEVICEREMOVEPENDING.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure identifiant l’appareil. La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil. Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true**.

## <a name="remarks"></a>Notes

Le système peut diffuser un \_ message DBT DEVICEREMOVEPENDING sans envoyer de message [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) correspondant. Dans ce cas, les applications et les pilotes doivent récupérer à partir de la perte de l’appareil le mieux possible.

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [traitement d’une demande de suppression d’un appareil](processing-a-request-to-remove-a-device.md).

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

[**\_HDR de diffusion dev \_**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> </dl>

 

 




