---
title: Message PBM_SETBARCOLOR (commctrl. h)
description: Définit la couleur de la barre de l’indicateur de progression dans le contrôle de barre de progression.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117717"
---
# <a name="pbm_setbarcolor-message"></a>\_Message PBM SETBARCOLOR

Définit la couleur de la barre de l’indicateur de progression dans le contrôle de barre de progression.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **COLORREF** qui spécifie la nouvelle couleur de barre de l’indicateur de progression. Si vous spécifiez la \_ valeur CLR par défaut, la barre de progression utilise sa couleur de barre d’indicateur de progression par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la couleur de la barre de l’indicateur de progression précédente, ou CLR \_ par défaut si la couleur de la barre de l’indicateur de progression est la couleur par défaut.

## <a name="remarks"></a>Notes

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





