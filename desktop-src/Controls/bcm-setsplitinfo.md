---
title: Message BCM_SETSPLITINFO (commctrl. h)
description: Définit des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la \_ macro Button SetSplitInfo.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512579"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Utilisez ce message uniquement avec les styles de boutons [**BS \_ SPLITBUTTON**](button-styles.md) et [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





