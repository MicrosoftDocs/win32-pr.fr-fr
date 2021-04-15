---
title: Code de notification EN_ENDCOMPOSITION (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur a entré de nouvelles données ou a fini d’entrer des données lors de l’utilisation de l’éditeur IME ou Text Services Framework.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- Contrôles Windows de code de notification EN_ENDCOMPOSITION
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
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464423"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

