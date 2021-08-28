---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration lorsque l’utilisateur double-clique sur l’icône d’une boîte de dialogue prise en charge par l’application.
title: Message CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9faf3f589e9e3e69c3b8df82bbb6eb2c075d6fba2836b9d8e773b392ad9385c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351349"
---
# <a name="cpl_dblclk-message"></a>\_Message DBLCLK cpl

Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration lorsque l’utilisateur double-clique sur l’icône d’une boîte de dialogue prise en charge par l’application.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numéro de la boîte de dialogue. Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lData* 
</dt> <dd>

Valeur que l’application du panneau de configuration a chargée dans le membre **lpData** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) de la boîte de dialogue. L’application charge le membre **lpData** en réponse au message [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, la valeur de retour est zéro ; dans le cas contraire, il est différent de zéro.

## <a name="remarks"></a>Remarques

En réponse à ce message, une application du panneau de configuration doit afficher la boîte de dialogue correspondante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPL \_ Sélectionner**](cpl-select.md)
</dt> </dl>

 

 
