---
title: Configuration et activation de la journalisation côté serveur
description: Configuration et activation de la journalisation côté serveur
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379918"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configuration et activation de la journalisation côté serveur

L’application active la journalisation sur la session du serveur ou le groupe d’URL avant d’envoyer la réponse avec [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). L’exemple suivant montre comment configurer et activer la journalisation côté serveur de type W3C :

1.  L’application initialise la structure [**des \_ \_ informations de journalisation http**](/windows/desktop/api/Http/ns-http-http_logging_info) avec **HttpLoggingTypeW3C** spécifié dans le membre de **format** et un masque de réinitialisation des constantes de [**\_ \_ champ de journal http**](http-log-field--constants.md) dans le membre **Fields** .
2.  L’application appelle [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) ou [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) avec **HttpServerLoggingProperty** spécifié dans le paramètre de *propriété* et un pointeur vers la structure d' [**\_ \_ informations de journalisation http**](/windows/desktop/api/Http/ns-http-http_logging_info) dans le paramètre *pPropertyInformation* .

Le masque de réfixe des constantes de [**\_ \_ champ de journal http**](http-log-field--constants.md) contient les champs qui peuvent être enregistrés dans le fichier journal W3C. Notez que la définition de la propriété **HttpServerLoggingProperty** sur une session serveur ou un groupe d’URL ne signifie pas que les réponses http seront journalisées. La journalisation est effectuée sur la base de la demande lorsque le W3C est activé dans l’appel à [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) ou [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

Pour activer la journalisation des réponses W3C pour chaque demande, l’application effectue les étapes suivantes :

1.  L’application initialise les membres des données des [**\_ champs du \_ \_ Journal http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) avec les informations de champ qui seront journalisées pour cette réponse.
2.  Le membre de **base. type** de la structure de [**\_ données de \_ champs \_ du journal http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) doit être initialisé à **HttpLogDataTypeFields**. Le champ **base. type** garantit l’extensibilité future de la structure et de l’API.
3.  L’application appelle [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) ou [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) avec un pointeur vers la structure de [**\_ données des \_ champs \_ du journal http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) dans le paramètre *pLogData* . L’application doit effectuer un cast du pointeur vers les [**\_ \_ données du journal PHTTP**](/windows/desktop/api/Http/ns-http-http_log_data).

 

 




