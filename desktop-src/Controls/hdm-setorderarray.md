---
title: Message HDM_SETORDERARRAY (commctrl. h)
description: Définit l’ordre de gauche à droite des éléments d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetOrderArray.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6218da9ec51e8bbce6aa928bdab203ca675426595d8e9bba476e511b84f4ea9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170959"
---
# <a name="hdm_setorderarray-message"></a>\_Message HDM SETORDERARRAY

Définit l’ordre de gauche à droite des éléments d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taille de la mémoire tampon au niveau de *lParam*, dans les éléments. Cette valeur doit être égale à la valeur retournée par [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau qui spécifie l’ordre dans lequel les éléments doivent être affichés, de gauche à droite. Par exemple, si le contenu du tableau est {2,0,1} , le contrôle affiche l’élément 2, l’élément 0 et l’élément 1, de gauche à droite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





