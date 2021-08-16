---
title: À propos de l’authentification mutuelle à l’aide de Kerberos
description: Dans l’authentification mutuelle, le client et le service doivent vérifier leurs identités respectives avant d’exécuter des fonctions d’application.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- À propos de l’authentification mutuelle à l’aide de Kerberos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b020b2d808cee96319cf411b4199bb4ff78f357cfdf8379f01c7d07bc1c5c1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841009"
---
# <a name="about-mutual-authentication-using-kerberos"></a>À propos de l’authentification mutuelle à l’aide de Kerberos

Dans l’authentification mutuelle, le client et le service doivent vérifier leurs identités respectives avant d’exécuter des fonctions d’application. Aucune des parties ne peut effectuer des opérations avec l’autre tant que l’identité n’a pas été vérifiée ; autrement dit, le service doit être en mesure de vérifier le client sans interroger le client et le client doit être en mesure de vérifier le service sans interroger le service.

La valeur d’un service qui peut authentifier un client est bien connue. Par exemple, un service de fichiers emprunte l’identité d’un client pour déterminer les fichiers auxquels le client peut accéder.

La valeur d’un client qui peut authentifier un service est moins comprise. L’authentification d’un service permet au client d’approuver les données qu’il obtient du service et d’être sécurisé lors de l’envoi de données sensibles au service. La capacité d’un client à authentifier un service est particulièrement importante dans les applications client/service qui prennent en charge la délégation du contexte de sécurité du client. autrement dit, le client autorise le service à agir en tant que délégué pour accéder à des services ou des ressources réseau supplémentaires.

Un service authentifie un client comme suit : le client établit un contexte de sécurité local soit en s’exécutant dans un contexte précédemment établi, par exemple dans la session d’un utilisateur connecté, soit en fournissant explicitement des informations d’identification au fournisseur de sécurité sous-jacent. Le service ne peut pas accepter les connexions à partir de n’importe quel client non authentifié.

Le mécanisme Kerberos par lequel un client authentifie un service fonctionne comme suit : lorsqu’un service est installé, un programme d’installation de service, exécuté avec des privilèges d’administrateur, inscrit un ou plusieurs noms de principal du service (SPN) uniques pour chaque instance de service. Les noms sont enregistrés dans le contrôleur de domaine Active Directory (DC) sur l’objet de compte d’utilisateur ou d’ordinateur que l’instance de service utilisera pour ouvrir une session. Lorsqu’un client demande une connexion à un service, il compose un SPN pour une instance de service, à l’aide des données connues ou des données fournies par l’utilisateur. Le client utilise ensuite le package SSPI Negotiate pour présenter le nom de principal du service au centre de distribution de clés (KDC) pour le compte de domaine client. Le KDC recherche dans la forêt un compte d’utilisateur ou d’ordinateur sur lequel le SPN est inscrit. Si le SPN est inscrit sur plusieurs comptes, l’authentification échoue. Dans le cas contraire, le centre KDC chiffre un message à l’aide du mot de passe du compte sur lequel le SPN a été inscrit. Le KDC transmet ce message chiffré au client, qui à son tour le transmet à l’instance de service. Le service utilise le package SSPI Negotiate pour déchiffrer le message, qu’il transmet au client et sur le KDC du client. Le KDC authentifie le service si le message déchiffré correspond à son message d’origine.

-   Pour plus d’informations sur la composition et l’inscription des noms de principal du service, consultez. [Noms de principal du service](service-principal-names.md)
-   pour plus d’informations et pour obtenir un exemple de code qui compose un SPN pour un service de sockets Windows qui se publie lui-même avec un point de connexion de service, consultez [composition des noms de principal du service pour un service avec SCP](composing-the-spns-for-a-service-with-an-scp.md).
-   Pour plus d’informations et pour obtenir un exemple de code qui compose un SPN pour un service RPC, consultez [composition de SPN pour un service RpcNs](composing-spns-for-an-rpcns-service.md).

 

 




