---
title: Windows Types de données du journal des événements (WinEvt. h)
description: Windows Le journal des événements définit les types de données suivants
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619989"
---
# <a name="windows-event-log-data-types"></a>Windows Types de données du journal des événements

Windows Le journal des événements définit les types de données suivants :


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_Gestionnaire evt**
</dt> <dd>

handle d’un objet de journal des événements Windows.

</dd> <dt>

**\_handle PEVT**
</dt> <dd>

pointeur vers le handle d’un objet de journal des événements Windows.

</dd> <dt>

**\_handle de \_ propriété du tableau d’objets evt \_ \_**
</dt> <dd>

handle d’un tableau d’objets du journal des événements Windows.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





