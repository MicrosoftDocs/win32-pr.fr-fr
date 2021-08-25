---
title: Configuration des timers larges de l’API du serveur HTTP
description: Configuration des timers larges de l’API du serveur HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047349"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Configuration des timers larges de l’API du serveur HTTP

Les minuteurs **HeaderWait** et **IDLECONNECTION** de l’API du serveur http sont configurés en appelant la fonction version 1,0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) . Le paramètre *ConfigId* est défini sur **HttpServiceConfigTimeout** et le paramètre *pConfigInformation* spécifie la structure de [**\_ \_ \_ \_ définition du délai d’attente de la configuration du service http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) qui contient la minuterie qui est définie et la valeur de la minuterie.

La configuration des délais d’expiration au niveau de l’API du serveur HTTP nécessite des privilèges d’administrateur, mais l’interrogation n’est pas possible. Ces configurations sont définies pour toutes les applications sur l’ordinateur et sont conservées lorsque le service HTTP est redémarré ou que l’ordinateur est redémarré. Pour interroger les délais d’expiration existants de l’API du serveur HTTP, l’application appelle [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




