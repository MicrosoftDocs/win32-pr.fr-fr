---
title: Message WM_CLEAR (winuser. h)
description: Une application envoie un \_ message WM Clear à un contrôle Edit ou à une zone de liste modifiable pour supprimer (effacer) la sélection actuelle, le cas échéant, du contrôle d’édition.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR des données de message Exchange
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008157"
---
# <a name="wm_clear-message"></a>\_Message d’effacement WM

Une application envoie un message **WM \_ Clear** à un contrôle Edit ou à une zone de liste modifiable pour supprimer (effacer) la sélection actuelle, le cas échéant, du contrôle d’édition.


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La suppression effectuée par le message **WM \_ Clear** peut être annulée en envoyant le contrôle d’édition à un message d' [**\_ annulation em**](../controls/em-undo.md) .

Pour supprimer la sélection actuelle et placer le contenu supprimé dans le presse-papiers, utilisez le message « [**WM \_ Cut**](wm-cut.md) ».

Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Clear** est géré par son contrôle d’édition. Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_copie WM**](wm-copy.md)
</dt> <dt>

[**découpe WM \_**](wm-cut.md)
</dt> <dt>

[**\_coller WM**](wm-paste.md)
</dt> <dt>

[**désannulation WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

