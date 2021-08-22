---
title: Code de notification EN_ENDCOMPOSITION (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur a entré de nouvelles données ou a fini d’entrer des données lors de l’utilisation de l’éditeur IME ou Text Services Framework.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9fe75910ea018cf9d72dd14696067eb0b2bc00dabd4456cca63e41a099a75d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436847"
---
# <a name="en_endcomposition-notification-code"></a>\_Code de notification en ENDCOMPOSITION

Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur a entré de nouvelles données ou a fini d’entrer des données lors de l’utilisation de l’éditeur IME ou [Text Services Framework](/windows/desktop/TSF/text-services-framework).


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) qui reçoit des informations sur la condition de fin de composition.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

