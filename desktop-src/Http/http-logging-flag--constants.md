---
title: Constantes HTTP_LOGGING_FLAG_ (http. h)
description: Définissez les options de configuration de la journalisation sur l’API du serveur HTTP.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742501"
---
# <a name="http_logging_flag_-constants"></a>\_ \_ Constantes d’indicateur de JOURNALisation http \_

Les constantes d' **\_ \_ indicateur \_ de journalisation http** définissent les options permettant de configurer la journalisation sur l’API du serveur http.

Ces constantes sont utilisées dans la structure des [**\_ \_ informations de journalisation http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_substitution de \_ l' \_ \_ heure locale \_ de l’indicateur de journalisation http**
</dt> <dd> <dl> <dt>



La substitution du fichier journal est basée sur l’heure locale. Par défaut, les substitutions de fichier journal sont basées sur le temps universel coordonné (UTC).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Protocole http \_ Indicateur de JOURNALisation \_ \_ utiliser la \_ \_ conversion UTF8**
</dt> <dd> <dl> <dt>



Les champs Unicode sont convertis en UTF8 multioctets lors de l’écriture dans les fichiers journaux. Par défaut, les fichiers journaux sont écrits avec la conversion de la page de codes locale.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**indicateur de journalisation HTTP- \_ \_ Erreurs de \_ journal \_ \_ uniquement**
</dt> <dd> <dl> <dt>



Les fichiers journaux contiennent uniquement des informations sur l’erreur. Par défaut, les réponses d’erreur et de réussite sont journalisées. Si l’indicateur de journalisation **http \_ \_ \_ ne consigne pas les \_ Erreurs \_ uniquement** ou si l’indicateur de journalisation http a le **succès du \_ \_ \_ journal \_ \_ uniquement** est défini, les informations d’erreur et de réussite sont consignées.

Cet indicateur ne peut pas être défini si l’indicateur de **\_ \_ \_ journalisation des échecs de journalisation http \_ \_ uniquement** est également défini. Ces deux indicateurs s’excluent mutuellement.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Protocole http \_ indicateur de journalisation- \_ \_ réussite du journal \_ \_ uniquement**
</dt> <dd> <dl> <dt>



Les fichiers journaux incluent uniquement des informations de réussite. Par défaut, les erreurs et les transactions de réussite sont journalisées. Si l’indicateur de journalisation **http \_ \_ \_ ne consigne pas les \_ Erreurs \_ uniquement** ou si l’indicateur de journalisation http a le **succès du \_ \_ \_ journal \_ \_ uniquement** est défini, les informations d’erreur et de réussite sont consignées.

Cet indicateur ne peut pas être défini si l’indicateur de **journalisation http indicateurs d' \_ \_ \_ \_ Erreurs \_ uniquement** est également défini. Ces deux indicateurs s’excluent mutuellement.


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

 

 





