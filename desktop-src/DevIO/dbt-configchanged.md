---
description: Le système diffuse l' \_ événement de l’appareil DBT CONFIGCHANGED pour indiquer que la configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion. Une application ou un pilote qui stocke des données dans le Registre sous la \_ clé de configuration HKEY Current \_ doit mettre à jour les données.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: Événement DBT_CONFIGCHANGED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114433"
---
# <a name="dbt_configchanged-event"></a>\_Événement DBT CONFIGCHANGED

Le système diffuse l' \_ événement de l’appareil DBT CONFIGCHANGED pour indiquer que la configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion. Une application ou un pilote qui stocke des données dans le Registre sous la \_ clé de configuration HKEY Current \_ doit mettre à jour les données.

Pour diffuser cet événement d’appareil, le système utilise le message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ CONFIGCHANGED et *lParam* défini sur zéro.


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

Définissez sur DBT \_ CONFIGCHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Définit la valeur zéro.

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

[**\_DEVICECHANGE WM**](wm-devicechange.md)
</dt> </dl>

 

 




