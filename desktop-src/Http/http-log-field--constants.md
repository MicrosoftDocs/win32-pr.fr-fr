---
title: Constantes HTTP_LOG_FIELD_ (http. h)
description: Définissez les champs dans le journal W3C et les journaux d’erreurs.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616caaed9829c7f926f95f8982033457e1835a6beccfcad8313f6624d68195db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950828"
---
# <a name="http_log_field_-constants"></a>\_ \_ Constantes de champ de journal http \_

Les constantes de **\_ \_ \_ champ de journal http** définissent les champs dans le journal W3C et les journaux d’erreurs.

Ces constantes sont utilisées dans la structure des [**\_ \_ informations de journalisation http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_date du \_ champ du journal http \_**
</dt> <dd> <dl> <dt>



Date à laquelle l’activité s’est produite.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_heure du \_ champ du journal http \_**
</dt> <dd> <dl> <dt>



Heure, au format UTC (temps universel coordonné), à laquelle l’activité s’est produite.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_IP du \_ client du champ du journal http \_ \_**
</dt> <dd> <dl> <dt>



Adresse IP du client à l’origine de la demande.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_nom d' \_ utilisateur du champ de journal http \_ \_**
</dt> <dd> <dl> <dt>



Nom de l’utilisateur authentifié qui a accédé à votre serveur. Les utilisateurs anonymes sont indiqués par un trait d'union.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_nom du \_ site du champ du journal http \_ \_**
</dt> <dd> <dl> <dt>



Nom du site sur lequel l’entrée de fichier journal a été générée.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Protocole http \_ \_nom d' \_ ordinateur \_ du champ de journal**
</dt> <dd> <dl> <dt>



Nom de l’ordinateur sur lequel l’entrée de fichier journal a été générée.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_ \_ \_ adresse IP du serveur de champs du journal http \_**
</dt> <dd> <dl> <dt>



Adresse IP du serveur sur lequel l’entrée de fichier journal a été générée.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_méthode de \_ champ de journal http \_**
</dt> <dd> <dl> <dt>



Action demandée, par exemple, une méthode d’extraction.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Protocole http \_ \_ \_ \_ ressource URI du champ de journal**
</dt> <dd> <dl> <dt>



La cible de l’action, par exemple, Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_ \_ requête URI de champ de journal http \_ \_**
</dt> <dd> <dl> <dt>



Requête, le cas échéant, que le client essayait d’exécuter. Une requête URI est nécessaire uniquement pour les pages dynamiques.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_État du \_ champ du journal http \_**
</dt> <dd> <dl> <dt>



Code d’état HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_ \_ État Win32 du champ de journal http \_ \_**
</dt> <dd> <dl> <dt>



code d’état Windows.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_octets du champ du journal http \_ \_ \_ envoyés**
</dt> <dd> <dl> <dt>



Nombre, en octets, envoyé par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_octets du champ du journal http \_ \_ \_ reçus**
</dt> <dd> <dl> <dt>



Nombre, en octets, reçu par le serveur.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_temps de champ du journal http \_ \_ \_ pris**
</dt> <dd> <dl> <dt>



Durée, en millisecondes, de l’action.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_port du \_ serveur de champs du journal http \_ \_**
</dt> <dd> <dl> <dt>



Numéro de port du serveur configuré pour le service.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Protocole http \_ \_ \_ \_ agent utilisateur du champ de journal**
</dt> <dd> <dl> <dt>



L’application utilisée par le client.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_cookie de \_ champ de journal http \_**
</dt> <dd> <dl> <dt>



Contenu du cookie envoyé ou reçu, le cas échéant.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_Référence du \_ champ de journal http \_**
</dt> <dd> <dl> <dt>



Site que l’utilisateur a visité pour la dernière fois. Ce site a fourni un lien vers le site actuel.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_version du \_ champ du journal http \_**
</dt> <dd> <dl> <dt>



Version du protocole HTTP utilisée par le client.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_hôte de \_ champ de journal http \_**
</dt> <dd> <dl> <dt>



Nom de l’en-tête de l’hôte, le cas échéant.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_sous- \_ État du champ du journal http \_ \_**
</dt> <dd> <dl> <dt>



Code d’erreur du sous-état.


</dt> </dl> </dd> </dl>

Les constantes suivantes sont utilisées pour la journalisation des erreurs HTTP.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_ \_ port client du champ du journal http \_ \_**
</dt> <dd> <dl> <dt>



Numéro de port du client à partir duquel la demande est reçue. Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI du \_ champ de journal http \_**
</dt> <dd> <dl> <dt>



URI reçu dans la demande, y compris la partie de la requête. Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ID de \_ site du champ du journal http \_ \_**
</dt> <dd> <dl> <dt>



ID numérique spécifique à l’application du groupe d’URL sur lequel la demande est routée. Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_raison du \_ champ du journal http \_**
</dt> <dd> <dl> <dt>



Expression de raison de l’erreur. Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_nom de \_ la \_ file d’attente du champ du journal http \_**
</dt> <dd> <dl> <dt>



Nom de la file d’attente de demandes vers laquelle la demande est distribuée. Ce champ de journal est utilisé uniquement pour la journalisation des erreurs.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_champ du journal http \_ \_ STREAMID**
</dt> <dd> <dl> <dt>



ID du flux.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de la version 2,0 de l’API du serveur HTTP](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_informations de journalisation http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





