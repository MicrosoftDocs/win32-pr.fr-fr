---
title: Message HDM_SETORDERARRAY (commctrl. h)
description: Définit l’ordre de gauche à droite des éléments d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetOrderArray.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY les contrôles de message Windows
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
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465479"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





