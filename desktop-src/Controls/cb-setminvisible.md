---
title: Message CB_SETMINVISIBLE (commctrl. h)
description: Une application envoie un \_ message CB SETMINVISIBLE pour définir le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9790c43141ef836c1dec86304f260b0490854b593b7005b594d2a718332296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063319"
---
# <a name="cb_setminvisible-message"></a>\_Message SETMINVISIBLE CB

Une application envoie un message **CB \_ SETMINVISIBLE** pour définir le nombre minimal d’éléments visibles dans la liste déroulante d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le nombre minimal d’éléments visibles.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message réussit, la valeur de retour est **true**. Sinon, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

Lorsque le nombre d’éléments dans la liste déroulante est supérieur au minimum, la zone de liste déroulante utilise une barre de défilement. Par défaut, 30 est le nombre minimal d’éléments visibles.

Ce message est ignoré si le contrôle de zone de liste déroulante a un [**\_ NOINTEGRALHEIGHT SCC**](combo-box-styles.md)de style.

Pour utiliser **CB \_ SETMINVISIBLE**, l’application doit spécifier comctl32.dll version 6 dans le manifeste. Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETMINVISIBLE CB**](cb-getminvisible.md)
</dt> <dt>

[**\_SetMinVisible ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





