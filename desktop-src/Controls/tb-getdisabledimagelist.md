---
title: Message TB_GETDISABLEDIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- TB_GETDISABLEDIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942020"
---
# <a name="tb_getdisabledimagelist-message"></a>TO \_ GETDISABLEDIMAGELIST message

Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images inactives, ou **null** si aucune liste d’images inactives n’est définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





