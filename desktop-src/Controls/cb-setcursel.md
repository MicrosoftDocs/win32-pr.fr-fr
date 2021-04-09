---
title: Message CB_SETCURSEL (winuser. h)
description: Une application envoie un \_ message CB SETCURSEL pour sélectionner une chaîne dans la liste d’une zone de liste déroulante.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032843"
---
# <a name="cb_setcursel-message"></a>\_Message SETCURSEL CB

Une application envoie un message **CB \_ SETCURSEL** pour sélectionner une chaîne dans la liste d’une zone de liste déroulante. Si nécessaire, la liste fait défiler la chaîne dans la vue. Le texte du contrôle d’édition de la zone de liste déroulante change pour refléter la nouvelle sélection, et toute sélection précédente dans la liste est supprimée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro de la chaîne à sélectionner. Si ce paramètre est défini sur-1, toute sélection en cours dans la liste est supprimée et le contrôle d’édition est effacé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est réussi, la valeur de retour est l’index de l’élément sélectionné. Si *wParam* est supérieur au nombre d’éléments dans la liste ou si *wParam* a la valeur-1, la valeur de retour est CB \_ Err et la sélection est désactivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_FindString CB**](cb-findstring.md)
</dt> <dt>

[**\_GETCURSEL CB**](cb-getcursel.md)
</dt> <dt>

[**\_SELECTSTRING CB**](cb-selectstring.md)
</dt> </dl>

 

 





