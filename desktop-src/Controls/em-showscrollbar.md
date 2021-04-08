---
title: Message EM_SHOWSCROLLBAR (RichEdit. h)
description: Affiche ou masque l’une des barres de défilement dans la fenêtre hôte d’un contrôle RichEdit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942025"
---
# <a name="em_showscrollbar-message"></a>\_Message SHOWSCROLLBAR em

Affiche ou masque l’une des barres de défilement dans la fenêtre hôte d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identifie la barre de défilement à afficher : horizontale ou verticale. Ce paramètre doit être **SB \_ vert** ou **SB \_ Horiz**.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie si la barre de défilement doit être affichée ou masquée. Spécifiez **true** pour afficher la barre de défilement et **false** pour la masquer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est valide uniquement lorsque le contrôle est actif sur place. Les appels effectués alors que le contrôle est inactif peuvent échouer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETSCROLLPOS em**](em-getscrollpos.md)
</dt> <dt>

[**\_SETSCROLLPOS em**](em-setscrollpos.md)
</dt> </dl>

 

 





