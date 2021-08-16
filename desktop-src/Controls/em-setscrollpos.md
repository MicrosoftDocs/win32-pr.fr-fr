---
title: Message EM_SETSCROLLPOS (RichEdit. h)
description: Fait défiler le contenu d’un contrôle Rich Edit jusqu’au point spécifié.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d86609c1b3f4b04ade24e5ea2f3343c367bbad0a52b8e07be7c18b2282536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412334"
---
# <a name="em_setscrollpos-message"></a>\_Message SETSCROLLPOS em

Fait défiler le contenu d’un contrôle Rich Edit jusqu’au point spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**point**](/previous-versions//dd162805(v=vs.85)) qui spécifie un point dans l’espace du texte virtuel du document, exprimé en pixels. Le document est défilant jusqu’à ce que ce point se trouve dans l’angle supérieur gauche de la fenêtre de contrôle d’édition. Si vous souhaitez modifier l’affichage de manière à ce que l’angle supérieur gauche de la vue comporte deux lignes et un caractère dans le bord gauche. Vous devez passer un point de (7, 22).

Le contrôle RichEdit vérifie les coordonnées x et y et les ajuste si nécessaire, afin qu’une ligne complète s’affiche en haut. Elle garantit également que le texte n’est jamais complètement défilant du rectangle d’affichage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne toujours la valeur 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETSCROLLPOS em**](em-getscrollpos.md)
</dt> </dl>

 

