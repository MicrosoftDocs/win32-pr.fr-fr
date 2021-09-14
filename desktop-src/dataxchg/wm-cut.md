---
title: Message WM_CUT (winuser. h)
description: Une application envoie un \_ message de coupe WM à un contrôle d’édition ou une zone de liste déroulante pour supprimer (couper) la sélection actuelle, le cas échéant, dans le contrôle d’édition et copier le texte supprimé dans le presse-papiers au \_ format de texte cf.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT des données de message Exchange
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095405"
---
# <a name="wm_cut-message"></a>\_Message de coupure WM

Une application envoie un message de **\_ coupe WM** à un contrôle d’édition ou une zone de liste déroulante pour supprimer (couper) la sélection actuelle, le cas échéant, dans le contrôle d’édition et copier le texte supprimé dans le presse-papiers au format de [**\_ texte CF**](standard-clipboard-formats.md) .


```C++
#define WM_CUT                          0x0300
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

La suppression effectuée par le message **WM \_ Cut** peut être annulée en envoyant le contrôle d’édition à un message d' [**\_ annulation em**](../controls/em-undo.md) .

Pour supprimer la sélection actuelle sans placer le texte supprimé dans le presse-papiers, utilisez le message [**WM \_ Clear**](wm-clear.md) .

Lorsqu’il est envoyé à une zone de liste déroulante, le message **WM \_ Cut** est géré par son contrôle d’édition. Ce message n’a aucun effet lorsqu’il est envoyé à une zone de liste déroulante avec le style [**\_ DropDownList SCC**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**WM- \_ Clear**](wm-clear.md)
</dt> <dt>

[**\_copie WM**](wm-copy.md)
</dt> <dt>

[**\_coller WM**](wm-paste.md)
</dt> <dt>

[**désannulation WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_Effacer em**](../controls/em-undo.md)
</dt> </dl>

 

