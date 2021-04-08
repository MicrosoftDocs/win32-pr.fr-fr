---
title: Types de données du journal des événements Windows (WinEvt. h)
description: 'Le journal des événements Windows définit les types de données suivants :'
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741388"
---
# <a name="windows-event-log-data-types"></a>Types de données du journal des événements Windows

Le journal des événements Windows définit les types de données suivants :


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_Gestionnaire evt**
</dt> <dd>

Handle d’un objet du journal des événements Windows.

</dd> <dt>

**\_handle PEVT**
</dt> <dd>

Pointeur vers le handle d’un objet du journal des événements Windows.

</dd> <dt>

**\_handle de \_ propriété du tableau d’objets evt \_ \_**
</dt> <dd>

Handle d’un tableau d’objets du journal des événements Windows.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





