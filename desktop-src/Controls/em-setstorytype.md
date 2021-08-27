---
title: Message EM_SETSTORYTYPE (RichEdit. h)
description: Définit le type d’histoire.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e09c62c50441857aac6f4018800de7a145081d64de49cdf7e9ca673a5370db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062879"
---
# <a name="em_setstorytype-message"></a>\_Message SETSTORYTYPE em

Définit le type d’histoire.


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’histoire.

</dd> <dt>

*lParam* 
</dt> <dd>

Type du nouveau récit. Pour obtenir la liste des types de récits, consultez [**em \_ GETSTORYTYPE**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type d’histoire qui a été défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





