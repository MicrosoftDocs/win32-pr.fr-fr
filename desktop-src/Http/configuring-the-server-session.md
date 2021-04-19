---
title: Configuration de la session serveur
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510799"
---
# <a name="configuring-the-server-session"></a>Configuration de la session serveur

L’ID de session du serveur est créé avec la fonction [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) et utilisé dans l’appel à [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). Le paramètre *pPropertyInformation* pointe vers la structure de configuration pour le type de propriété défini. Le paramètre *PropertyInformationLength* spécifie la taille, en octets, de la structure de configuration. Par exemple, lors de la définition du **HttpServerTimeoutsProperty** , le paramètre **pPropertyInformation** doit pointer vers une mémoire tampon qui correspond au moins à la taille de la structure d' [**informations de limite du délai d' \_ expiration \_ \_ http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

En général, une application HTTP crée une session de serveur unique et peut définir des propriétés à l’échelle de l’application, telles que la limite de limitation de bande passante globale, ou activer la journalisation centralisée sur cette session serveur. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) remplace les configurations de l’API du serveur http pour l’application appelante ; elle n’affecte pas les propriétés de l’API du serveur HTTP. Les configurations de session serveur sont interrogées en appelant [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




