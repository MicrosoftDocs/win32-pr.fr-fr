---
title: HTTP_RESPONSE (http. h)
description: 'La version de la \_ structure de réponse http dépend de la version de la file d’attente des demandes utilisée comme suit : API de serveur http version 1,0 de la file d’attente de demandes. il s’agit d’une \_ structure de requête HTTP \_ v1. API serveur HTTP version 2,0 file d’attente de demandes il s’agit d’une \_ structure de requête HTTP \_ v2.'
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384399"
---
# <a name="http_response"></a>\_réponse http

La version de la structure de **\_ réponse http** dépend de la version de la file d’attente de demandes utilisée comme suit :

-   API de serveur HTTP version 1,0 file d’attente de requêtes : il s’agit d’une structure de [**\_ requête HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .
-   API de serveur HTTP version 2,0 file d’attente de requêtes : il s’agit d’une structure de [**\_ requête HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .

N’utilisez pas [**la \_ requête HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) et la [**\_ requête HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) directement dans votre code ; à la place, l’utilisation de la **\_ réponse http** garantit que la version appropriée de la structure est utilisée en fonction de la version de la file d’attente des demandes.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**\_réponse http**
</dt> <dd>

La demande provient d’une file d’attente de demandes v1.

</dd> <dt>

**\_réponse http**
</dt> <dd>

La demande provient d’une file d’attente de demandes v2.

</dd> <dt>

**\_réponse PHTTP**
</dt> <dd>

Pointeur vers une structure de **\_ réponse http** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Http. h</dt> </dl> |



 

 





