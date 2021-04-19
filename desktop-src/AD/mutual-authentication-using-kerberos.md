---
title: Authentification mutuelle à l'aide de Kerberos
description: L’authentification mutuelle est une fonctionnalité de sécurité dans laquelle un processus client doit prouver son identité à un service, et le service doit prouver son identité au client, avant qu’un trafic d’application ne soit transmis via la connexion client/service.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, authentification mutuelle
- Active Directory, utilisation de, sécurité, authentification mutuelle
- sécurité AD
- sécurité AD, authentification mutuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "106518000"
---
# <a name="mutual-authentication-using-kerberos"></a>Authentification mutuelle à l'aide de Kerberos

L’authentification mutuelle est une fonctionnalité de sécurité dans laquelle un processus client doit prouver son identité à un service, et le service doit prouver son identité au client, avant qu’un trafic d’application ne soit transmis via la connexion client/service.

Active Directory Domain Services et Windows assurent la prise en charge des noms de principal du service (SPN), qui sont un composant clé du mécanisme Kerberos par lequel un client authentifie un service. Un SPN est un nom unique qui identifie une instance d’un service et qui est associé au compte d’ouverture de session sous lequel l’instance de service s’exécute. Les composants d’un SPN sont tels qu’un client peut composer un SPN pour un service sans le compte d’ouverture de session du service. Cela permet au client de demander au service d’authentifier son compte même si le client n’a pas le nom du compte.

Cette section comprend une vue d’ensemble des éléments suivants :

-   Authentification mutuelle à l’aide de Kerberos.
-   Composition d’un nom principal de service unique.
-   Comment un programme d’installation de service inscrit des noms de principal du service sur l’objet de compte associé à une instance de service.
-   Comment une application cliente utilise l’objet point de connexion de service (SCP) d’une instance de service dans Active Directory Domain Services pour récupérer des données à partir desquelles composer un SPN pour le service.
-   Comment une application cliente utilise un SPN de service conjointement avec l’interface SSPI (Security Support Provider Interface) pour authentifier le service.
-   Exemple de code pour une application cliente/service Windows Sockets qui utilise un SCP et un SSPI pour effectuer une authentification mutuelle.
-   Exemple de code pour un client/service RPC qui effectue une authentification mutuelle à l’aide du service de noms RPC et de l’authentification RPC.
-   Comment un service d’inscription et de résolution Windows Sockets (RnR) utilise des noms de principal du service (SPN) pour effectuer une authentification mutuelle.

Cette section décrit l’utilisation de domaine Active Directory Service pour l’authentification mutuelle, en particulier l’objectif des points de connexion de service et des noms de principal du service dans l’authentification mutuelle. Il ne s’agit pas d’une description complète de l’utilisation de SSPI pour l’authentification mutuelle ou du support d’authentification et de sécurité disponible pour les applications RPC et Windows Sockets.

Pour plus d’informations, consultez :

-   [Publication avec des points de connexion de service](publishing-with-service-connection-points.md)
-   [SSPI](/windows/desktop/SecAuthN/sspi)
-   [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [RPC](/windows/desktop/Rpc/rpc-start-page)

 

 