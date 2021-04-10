---
title: Message PBM_GETRANGE (commctrl. h)
description: Récupère des informations sur les limites haute et basse actuelles d’un contrôle de barre de progression donné.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942474"
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

## <a name="return-value"></a>Valeur retournée

Retourne un entier qui représente la valeur limite spécifiée par *wParam*. Si *lParam* n’est pas **null**, *lParam* doit pointer vers une structure [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) qui doit être remplie avec les deux valeurs limites.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





