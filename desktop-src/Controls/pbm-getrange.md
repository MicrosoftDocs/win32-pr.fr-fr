---
title: Message PBM_GETRANGE (commctrl. h)
description: Récupère des informations sur les limites haute et basse actuelles d’un contrôle de barre de progression donné.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117726"
---
# <a name="pbm_getrange-message"></a>\_Message PBM GETRANGE

Récupère des informations sur les limites haute et basse actuelles d’un contrôle de barre de progression donné.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de l’indicateur spécifiant la valeur limite à utiliser comme valeur de retour du message. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                    | Signification                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VRAI * * * * *</dt> </dl>    | Retourne la limite inférieure.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSe * * * * *</dt> </dl> | Retourne la limite supérieure.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) qui doit être remplie avec les limites haute et basse du contrôle de barre de progression. Si ce paramètre a la valeur **null**, le contrôle ne retourne que la limite spécifiée par *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un entier qui représente la valeur limite spécifiée par *wParam*. Si *lParam* n’est pas **null**, *lParam* doit pointer vers une structure [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) qui doit être remplie avec les deux valeurs limites.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





