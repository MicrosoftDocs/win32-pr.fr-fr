---
description: Avertit un appbar lorsqu’une application en plein écran est en mode d’ouverture ou de fermeture. Cette notification est envoyée sous la forme d’un message défini par l’application qui est défini par le \_ nouveau message ABM.
title: Message ABN_FULLSCREENAPP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 55bba51153ff90dfa69b870468a1c5002121eaccf45559821c6031aba35d4b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090789"
---
# <a name="abn_fullscreenapp-message"></a>Message d’ABN \_ FULLSCREENAPP

Avertit un appbar lorsqu’une application en plein écran est en mode d’ouverture ou de fermeture. Cette notification est envoyée sous la forme d’un message défini par l’application qui est défini par [**le \_ nouveau message ABM**](abm-new.md) .


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fOpen* 
</dt> <dd>

Indicateur spécifiant si une application en plein écran est en mode d’ouverture ou de fermeture. Ce paramètre a la **valeur true** si l’application s’ouvre ou **false** si elle est en fermeture.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Lors de l’ouverture d’une application en plein écran, un appbar doit se placer au bas de l’ordre de plan. Lorsqu’il se ferme, appbar doit restaurer sa position dans l’ordre de plan.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




