---
title: Création d’un client
description: La création d’un client pour les services Web est considérablement simplifiée dans WWSAPI par l’API de modèle de service et l’outil WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380376"
---
# <a name="creating-a-client"></a>Création d’un client

La création d’un client pour les services Web est considérablement simplifiée dans WWSAPI par l’API de [modèle de service](service-model-layer-overview.md) et l’outil [WsUtil.exe](wsutil-compiler-tool.md) . Le modèle de service fournit une API qui permet au client d’envoyer et de recevoir des [messages](message.md) sur un [canal](channel.md) en tant qu’appels de méthode C. L’outil WsUtil génère des en-têtes et des assistances pour l’implémentation du client. Ces en-têtes incluent les types et les prototypes de fonction pour les fonctions C représentant les services offerts par le service Web cible. Les applications auxiliaires sont utilisées pour créer le proxy de service, qui contient les informations de liaison et l' [adresse de point de terminaison](endpoint-address.md) pour le service.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Utilisation de WsUtil pour générer des en-têtes et des assistances

Pour générer les en-têtes et les aiders, WsUtil ouvre et lit les fichiers de métadonnées du service cible (fichiers WSDL et XSD) et les convertit en en-têtes. par conséquent, il est nécessaire de récupérer les fichiers de métadonnées pour le service cible à l’avance, par exemple à l’aide de SvcUtil, une partie du Windows Communication Foundation. Pour des raisons de sécurité, il est impératif que vos copies de ces fichiers soient dignes de confiance. (Pour plus d’informations, consultez la section « sécurité » de la rubrique de l' [outil compilateur WsUtil](wsutil-compiler-tool.md) .)

Pour exécuter WsUtil, utilisez la syntaxe de ligne de commande suivante si les fichiers WSDL et XSD du service se trouvent dans leur propre répertoire : `WsUtil.exe *.wsdl *.xsd` . Vous pouvez également spécifier les fichiers par nom complet.

WsUtil génère généralement deux fichiers pour chaque fichier de métadonnées : un en-tête et un fichier C. Ajoutez ces fichiers à votre projet de codage et utilisez les \# instructions include pour les inclure dans le code de votre client. (Les fichiers XSD représentent des types, et les fichiers WSDL représentent des opérations.)

## <a name="creating-the-service-proxy"></a>Création du proxy de service

L’en-tête généré par WsUtil contient une routine d’assistance pour la création du proxy de service avec la liaison requise. Cette routine est incluse dans la section « routines d’assistance de la stratégie » du fichier d’en-tête généré. Par exemple, l’en-tête généré pour le service de calculatrice illustré dans l’exemple [httpcalculatorclientexample](httpcalculatorclientexample.md) contient le prototype de fonction suivant.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorporez cette application d’assistance dans votre code et transmettez un handle de [ \_ \_ proxy de service Web](ws-service-proxy.md) pour recevoir le descripteur du proxy de service créé. Dans le scénario le plus simple, dans lequel seul un handle de proxy de service et un objet d’erreur sont passés à la fonction, l’appel ressemble à ce qui suit.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Pour créer la partie adresse du proxy de service, appelez [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) avec un handle vers le proxy de service et un pointeur vers [**une \_ \_ adresse de point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenant l’adresse de point de terminaison de service à laquelle vous souhaitez vous connecter.

## <a name="implementing-the-client-with-function-prototypes"></a>Implémentation du client à l’aide de prototypes de fonction

Les en-têtes générés à partir des fichiers WSDL de service contiennent également des prototypes de fonction C représentant les services disponibles à partir du service Web et spécifiques à la liaison requise. Par exemple, un en-tête généré pour le service de calculatrice illustré dans HttpCalculatorServiceExample contient le prototype suivant pour l’opération de multiplication de ce service.

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

Vous pouvez copier les prototypes et les utiliser en tant que modèles pour coder les appels de fonction dans votre client, dans chaque cas en passant le handle au proxy de service. Lorsque vous avez terminé avec le proxy de service, appelez [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).

 

 




