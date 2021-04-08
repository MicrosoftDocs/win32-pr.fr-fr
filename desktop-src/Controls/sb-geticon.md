---
title: Message SB_GETICON (commctrl. h)
description: Récupère l’icône pour un composant dans une barre d’État.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844002"
---
# <a name="sb_geticon-message"></a>\_Message SB GETICON

Récupère l’icône pour un composant dans une barre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la partie qui contient l’icône à récupérer. Si ce paramètre a la valeur-1, la barre d’État est supposée être une barre d’état de [mode simple](status-bars.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de l’icône en cas de réussite, ou **null** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





