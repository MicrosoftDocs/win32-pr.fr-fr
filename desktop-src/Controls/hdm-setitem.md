---
title: Message HDM_SETITEM (commctrl. h)
description: Définit les attributs de l’élément spécifié dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetItem.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006262"
---
# <a name="hdm_setitem-message"></a>\_Message HDM SETITEM

Définit les attributs de l’élément spécifié dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index actuel de l’élément dont les attributs doivent être modifiés.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) qui contient des informations d’élément. Lorsque ce message est envoyé, le membre de **masque** de la structure doit être défini pour indiquer les attributs qui sont définis.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

La structure [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) qui prend en charge ce message prend en charge les informations sur l’ordre des éléments et la liste d’images. À l’aide de ces membres, vous pouvez contrôler l’ordre dans lequel les éléments sont affichés et spécifier les images à afficher avec les éléments.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) et **HDM \_ SETITEMA** (ANSI)<br/>                   |



 

 





