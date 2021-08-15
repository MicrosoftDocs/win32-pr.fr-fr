---
title: Message HDM_HITTEST (commctrl. h)
description: Teste un point pour déterminer l’élément d’en-tête, le cas échéant, à l’emplacement spécifié.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc219640d9dd9d5d9a4c9537169401f681e37660554266b3edd653365cf8cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544769"
---
# <a name="hdm_hittest-message"></a>\_Message HDM HITTEST

Teste un point pour déterminer l’élément d’en-tête, le cas échéant, à l’emplacement spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) qui contient la position à tester et reçoit des informations sur les résultats du test.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément à la position spécifiée, le cas échéant, ou 1 dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





