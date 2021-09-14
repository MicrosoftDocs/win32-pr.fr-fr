---
description: Le système diffuse l’événement de l' \_ appareil DBT DEVICEQUERYREMOVE pour demander l’autorisation de supprimer un appareil ou un élément multimédia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: Événement DBT_DEVICEQUERYREMOVE (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114426"
---
# <a name="dbt_devicequeryremove-event"></a>\_Événement DBT DEVICEQUERYREMOVE

Le système diffuse l’événement de l' \_ appareil DBT DEVICEQUERYREMOVE pour demander l’autorisation de supprimer un appareil ou un élément multimédia. Ce message est la dernière chance pour les applications et les pilotes de se préparer pour cette suppression. Toutefois, toute application peut refuser cette demande et annuler l’opération.

Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEQUERYREMOVE et *lParam* défini comme indiqué ci-dessous.


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

Définissez sur DBT \_ DEVICEQUERYREMOVE.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure identifiant l’appareil à supprimer. La structure se compose d’un en-tête indépendant des événements, suivi de membres dépendants de l’événement qui décrivent l’appareil. Pour utiliser cette structure, traitez la structure comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) , puis vérifiez son membre **dbch \_ DeviceType** pour déterminer le type d’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour accorder l’autorisation de supprimer un appareil.

Retournez \_ la requête de diffusion \_ Deny pour refuser l’autorisation de supprimer un appareil.

## <a name="remarks"></a>Notes

Vous devez fermer tous les descripteurs de l’appareil, sinon la suppression de l’appareil échouera.

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

 

 




