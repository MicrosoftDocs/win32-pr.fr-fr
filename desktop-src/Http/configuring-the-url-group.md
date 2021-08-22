---
title: Configuration du groupe d’URL
description: Configuration du groupe d’URL
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d335af063eb8cadc557db3f01da850b468099866e292bcd5ea2a3af314de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014907"
---
# <a name="configuring-the-url-group"></a>Configuration du groupe d’URL

L’ID de groupe d’URL est créé avec la fonction [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) et utilisé dans l’appel à [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). Le paramètre *pPropertyInformation* pointe vers la structure de configuration pour le type de propriété défini. Le paramètre **PropertyInformationLength** spécifie la taille, en octets, de la structure de configuration. Par exemple, lors de la définition du **HttpServerTimeoutsProperty** , le paramètre *pPropertyInformation* doit pointer vers une mémoire tampon qui ne peut pas être inférieure à la structure [**\_ d' \_ \_ informations de limite de dépassement de délai http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) . Les configurations de groupe d’URL sont interrogées en appelant [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Une fois le groupe d’URL créé, les URL sont ajoutées au groupe avec [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). Le groupe d’URL doit être associé à une file d’attente de demandes de la version 2,0 pour recevoir des demandes. Pour associer le groupe d’URL à une file d’attente de demandes, l’application appelle [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) et spécifie **HttpServerBindingProperty** dans le paramètre *Property* . Si cette propriété n’est pas définie, les demandes de correspondance pour le groupe d’URL ne sont pas remises dans une file d’attente de demandes et l’API du serveur HTTP génère une réponse 503. L’application peut uniquement ajouter des URL qui ont été précédemment réservées avec le service à un groupe d’URL lors de l’exécution avec un privilège faible. Pour plus d’informations, consultez la rubrique [réservation d’espace de noms, inscriptions et routage](namespace-reservations-registrations-and-routing.md) .

 

 




