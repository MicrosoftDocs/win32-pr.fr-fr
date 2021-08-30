---
title: CBN_CLOSEUP le code de notification (winuser. h)
description: Envoyé lorsque la zone de liste d’une zone de liste déroulante a été fermée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ff96f30a13705028a18199780da69948633c0c3381d87896f1c7137ae06041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085769"
---
# <a name="cbn_closeup-notification-code"></a>\_Code de notification CBN gros plan

Envoyé lorsque la zone de liste d’une zone de liste déroulante a été fermée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la zone de liste déroulante.

</dd> </dl>

## <a name="remarks"></a>Remarques

Si l’utilisateur a modifié la sélection actuelle, la zone de liste déroulante envoie également le code de notification [CBN \_ selChange](cbn-selchange.md) lorsque la liste déroulante se ferme. En général, vous ne pouvez pas prédire l’ordre dans lequel les codes de notification seront envoyés. En particulier, un \_ Code de notification CBN selChange peut se produire avant ou après un \_ Code de notification CBN gros plan.

Pour exécuter un processus spécifique chaque fois que l’utilisateur sélectionne un élément de liste, vous pouvez gérer le code de notification [CBN \_ selChange](cbn-selchange.md) ou CBN \_ gros plan. En général, vous attendez le code de \_ notification CBN gros plan avant de traiter une modification dans la sélection actuelle. Cela peut être particulièrement important si une quantité importante de traitement est nécessaire.

Ce code de notification n’est pas envoyé à une zone de liste déroulante avec le style [**CBS \_ simple**](combo-box-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[\_liste déroulante CBN](cbn-dropdown.md)
</dt> <dt>

[CBN \_ selChange](cbn-selchange.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

