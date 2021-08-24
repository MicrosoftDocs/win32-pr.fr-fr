---
title: Configuration de l’installation
description: La configuration du programme d’installation requiert des privilèges d’administrateur et est persistante entre les redémarrages.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d59065ff34e7998d9df0503f6ae7503d9d402def6053f8176ba5af5b6a9efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996116"
---
# <a name="setup-configuration"></a>Configuration de l’installation

La configuration du programme d’installation requiert des privilèges d’administrateur et est persistante entre les redémarrages. En règle générale, une application de configuration s’exécutant avec des privilèges d’administrateur effectue une telle configuration permanente lors de l’installation afin que les applications puissent s’exécuter avec des privilèges inférieurs, bien que la configuration persistante puisse être effectuée à tout moment. La configuration de l’installation peut inclure l’une des quatre activités suivantes :

-   Création d’une réservation d’URL. L’API HTTP permet à l’application d’installation de réserver des préfixes d’URL pour les files d’attente de requêtes associées à des applications spécifiques. Pour réserver une URL, l’application d’installation appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) avec le paramètre *ConfigId* défini sur **HttpServiceConfigUrlAclInfo** et passe un pointeur dans le paramètre *pConfigInformation* à une [**configuration de \_ service http \_ \_ URLACL \_ définir**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) la structure contenant les informations d’inscription. Pour plus d’informations, consultez [Réservations d’espaces de noms, inscriptions et routage](namespace-reservations-registrations-and-routing.md).
-   Configuration de SSL. Pour configurer SSL, l’administrateur appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) avec le paramètre *ConfigId* défini sur **HttpServiceConfigSSLCertInfo** et transmet un pointeur dans le paramètre *pConfigInformation* à une structure SSL de [**configuration de service http contenant les informations \_ \_ \_ \_**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) de certificat SSL.
-   Définition d’autres configurations persistantes du serveur HTTP, telles que les adresses IP sur lesquelles le serveur HTTP écoute et la valeur du délai d’attente à l’ensemble du serveur. Consultez [liste d’écoute IP](ip-listen-list.md) et [**\_ \_ \_ délai d’expiration \_ de la configuration du service http défini**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




