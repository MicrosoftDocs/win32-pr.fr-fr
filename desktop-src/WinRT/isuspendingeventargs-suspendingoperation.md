---
description: Obtient l’opération d’interruption de l’application.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'ISuspendingEventArgs :: SuspendingOperation, propriété (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: a798f91c0fd9ec20da61685a29120106c0eaaa4804521bb5ec5f931291372c2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121549"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a>ISuspendingEventArgs :: SuspendingOperation, propriété

Obtient l’opération d’interruption de l’application.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Opération de suspension.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| En-tête<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 




