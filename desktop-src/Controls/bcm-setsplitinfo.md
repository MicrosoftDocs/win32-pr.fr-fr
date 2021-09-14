---
title: Message BCM_SETSPLITINFO (commctrl. h)
description: Définit des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920387"
---
# <a name="bcm_setsplitinfo-message"></a>\_Message SETSPLITINFO BCM

Définit des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ SPLITINFO de bouton**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) contenant des informations sur le bouton partagé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Utilisez ce message uniquement avec les styles de boutons [**BS \_ SPLITBUTTON**](button-styles.md) et [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





