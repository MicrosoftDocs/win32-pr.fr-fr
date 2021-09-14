---
description: Avertit un appbar que l’état d’affichage automatique ou de masquage automatique de la barre des tâches a changé&\# 8212 ; autrement dit, l’utilisateur a sélectionné ou désactivé la &\# 0034 ; Always on&\# 0034 ; ou &\# 0034 ; Masquer automatiquement&\# 0034 ; case à cocher dans la feuille de propriétés de la barre des tâches.
title: Message ABN_STATECHANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227012"
---
# <a name="abn_statechange-message"></a>\_Message ABN STATECHANGE

Avertit un appbar que l’état d’affichage automatique ou de masquage automatique de la barre des tâches a changé. autrement dit, l’utilisateur a activé ou désactivé la case à cocher « toujours visible » ou « masquer automatiquement » dans la feuille de propriétés de la barre des tâches.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Paramètres

Ce message n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Un appbar peut utiliser ce message de notification pour définir son état sur conforme à celui de la barre des tâches, si vous le souhaitez.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




