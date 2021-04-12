---
description: Le type de données de contexte de l' \_ énumération SCE \_ est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par la \_ fonction PFSCE Query \_ info pour naviguer dans la base de données de sécurité.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318222"
---
# <a name="sce_enumeration_context"></a>\_contexte d’énumération SCE \_

Le type de données de contexte de l' **\_ \_ énumération SCE** est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par la fonction [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) pour naviguer dans la base de données de sécurité.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations sur la requête PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

