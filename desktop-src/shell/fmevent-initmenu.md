---
description: Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne le menu de l’extension à partir de la barre de menus du gestionnaire de fichiers. L’extension peut utiliser cette notification pour initialiser les éléments de menu.
title: Message FMEVENT_INITMENU (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 77b9aa668087f0c02042ccb7e5b822f68596404761d53ec682c76ef98d46c18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459046"
---
# <a name="fmevent_initmenu-message"></a>\_Message FMEVENT INITMENU

Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne le menu de l’extension à partir de la barre de menus du gestionnaire de fichiers. L’extension peut utiliser cette notification pour initialiser les éléments de menu.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*HMENU* 
</dt> <dd>

Handle vers la barre de menus du gestionnaire de fichiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une DLL d’extension doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Une DLL d’extension reçoit ce message uniquement lorsque l’utilisateur sélectionne le menu de niveau supérieur. Si l’extension contient des sous-menus, elle doit être initialisée en même temps qu’elle Initialise le menu de niveau supérieur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




