---
title: Message BCM_GETSPLITINFO (commctrl. h)
description: Obtient des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la \_ macro Button GetSplitInfo.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ee0771c8999c6a805931a93ed28c245082d18e538856fde42b69622ee73f9a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921639"
---
# <a name="bcm_getsplitinfo-message"></a>\_Message GETSPLITINFO BCM

Obtient des informations pour un contrôle bouton partagé. Envoyez ce message explicitement ou à l’aide de la macro [**Button \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**\_ SPLITINFO de bouton**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) pour recevoir des informations sur le bouton. L’appelant est chargé d’allouer la mémoire pour la structure. Définissez le membre de **masque** de cette structure pour déterminer les informations à recevoir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Utilisez ce message uniquement avec les styles de boutons [**BS \_ SPLITBUTTON**](button-styles.md) et [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Configuration requise



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

**Méthodologique**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





