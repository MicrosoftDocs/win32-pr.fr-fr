---
title: Constantes HTTP_AUTH_ENABLE_ (http. h)
description: Définir les schémas d’authentification qui peuvent être activés sur un groupe d’URL.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466790"
---
# <a name="http_auth_enable_-constants"></a>\_ \_ Constantes d’activation de l’authentification http \_

Les constantes d' **\_ \_ activation** de l’authentification http définissent les schémas d’authentification qui peuvent être activés sur un groupe d’URL.

Ces constantes sont utilisées dans la structure des [**\_ \_ \_ informations d’authentification du serveur http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_authentification http \_ activée de \_ base**
</dt> <dd> <dl> <dt>



Le schéma d’authentification de base est activé.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**Digest d’activation de l' \_ authentification http \_ \_**
</dt> <dd> <dl> <dt>



Le schéma d’authentification Digest est activé.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_authentification http \_ Enable \_ Kerberos**
</dt> <dd> <dl> <dt>



Le schéma d’authentification Kerberos est activé.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP \_ auth \_ ex \_ Flag \_ activer \_ \_ \_ la mise en cache des informations d’identification Kerberos**
</dt> <dd> <dl> <dt>



La mise en cache des informations d’identification Kerberos est activée.

**Windows Server 2003 et antérieur :** Non disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_ \_ \_ \_ \_ informations d’identification de capture d’indicateur http auth ex**
</dt> <dd> <dl> <dt>



L’API du serveur HTTP capture l’identité de l’appelant et l’utilise pour l’authentification uniquement pour les schémas Negotiate et Kerberos.

**Windows Server 2003 et antérieur :** Non disponible.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_authentification http \_ activer \_ NTLM**
</dt> <dd> <dl> <dt>



Le schéma d’authentification NTLM est activé.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP \_ auth \_ activer \_ Negotiate**
</dt> <dd> <dl> <dt>



Le schéma d’authentification Negotiate est activé.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP \_ auth \_ activer \_ tout**
</dt> <dd> <dl> <dt>



Tous les schémas d’authentification sont activés.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de la version 2,0 de l’API du serveur HTTP](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_ \_ informations d’authentification du serveur http \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





