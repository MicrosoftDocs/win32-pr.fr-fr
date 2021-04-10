---
description: La \_ notification SPFILENOTIFY ENDSUBQUEUE est envoyée à la fonction de rappel lorsque la file d’attente effectue toutes les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Message d’SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042766"
---
# <a name="spfilenotify_endsubqueue-message"></a>\_Message SPFILENOTIFY ENDSUBQUEUE

La notification **SPFILENOTIFY \_ ENDSUBQUEUE** est envoyée à la fonction de rappel lorsque la file d’attente effectue toutes les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Sous-file d’attente qui s’est terminée. Ce paramètre peut prendre l’une des valeurs suivantes FILEOP \_ Delete, FILEOP \_ Rename ou FILEOP \_ Copy.

</dd> <dt>

*Param2* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




