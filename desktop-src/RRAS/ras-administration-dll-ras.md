---
title: DLL d’administration RAS
description: La DLL exporte les fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6be479d00175750fb4d6ffce73aab4439d2c7df9e6e07f97e9964f267ce82a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909919"
---
# <a name="ras-administration-dll"></a>DLL d’administration RAS

La DLL exporte les fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter. Vous pouvez utiliser la DLL pour effectuer les fonctions d’administration suivantes :

-   Décidez s’il faut autoriser un utilisateur à se connecter au serveur. Cela peut fournir une vérification de sécurité en plus de l’authentification utilisateur RAS standard.
-   Enregistrez l’heure à laquelle chaque utilisateur se connecte et se déconnecte du serveur. Cela peut être utile à des fins de facturation ou d’audit.
-   Attribuez une adresse IP à chaque utilisateur. Cela peut être utile pour des raisons de sécurité afin de mapper la connexion d’un utilisateur à un ordinateur spécifique.

Implémentez les fonctions suivantes lors du développement d’une DLL d’administration de serveur RAS.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Une DLL d’administration RAS doit implémenter et exporter toutes les fonctions ci-dessus. Si l’une des fonctions n’est pas implémentée, le démarrage du service d’accès à distance échoue.

Les fonctions [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) et [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) permettent à la dll d’auditer les connexions utilisateur au serveur. un serveur RAS Windows NT/Windows 2000 appelle la fonction **RasAdminAcceptNewConnection** chaque fois qu’un utilisateur tente de se connecter. La fonction peut empêcher l’utilisateur de se connecter. Vous pouvez également utiliser la fonction pour générer une entrée dans un journal pour la facturation ou l’audit. Lorsque l’utilisateur se déconnecte, le serveur RAS appelle la fonction **RasAdminConnectionHangupNotification** , qui peut consigner l’heure à laquelle l’utilisateur s’est déconnecté.

Une fois que le serveur RAS a authentifié un appelant, il appelle la fonction [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) pour obtenir une adresse IP pour le client distant. La DLL peut utiliser cette fonction pour fournir un autre schéma de mappage d’une adresse IP à un utilisateur d’accès à distance. Si **RasAdminGetIpAddressForUser** n’est pas implémenté, un serveur RAS connecte un utilisateur distant à une adresse IP sélectionnée à partir d’un pool statique d’adresses IP, ou une option sélectionnée par un serveur DHCP (Dynamic Host Configuration Protocol). La fonction **RasAdminGetIpAddressForUser** permet à la dll de remplacer cette adresse IP par défaut et de spécifier une adresse IP spécifique pour chaque utilisateur. La fonction **RasAdminGetIpAddressForUser** peut définir un indicateur qui force RAS à appeler la fonction [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) lorsque l’utilisateur se déconnecte. La DLL peut utiliser [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) pour mettre à jour son mappage utilisateur-adresse IP.

RAS sérialise les appels dans la DLL d’administration. Un appel à l’une des fonctions de la DLL pour un client RAS donné n’est jamais devancé par un appel à cette fonction pour un autre client RAS. l’appel initial est garanti être terminé avant que RAS appelle la fonction pour l’autre client. En outre, la sérialisation s’étend à certains groupes de fonctions. Les fonctions d’adresse IP sont sérialisées en tant que groupe ; un appel dans [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) ou [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) bloquera les appels jusqu’à ce que l’appel initial soit terminé. [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) et [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) sont également sérialisés en tant que groupe.

RAS exécute les fonctions permettant d’attribuer des adresses IP dans un processus et exécute les fonctions pour les notifications de connexion et de déconnexion dans un autre processus. Par conséquent, la DLL ne doit pas dépendre des données partagées entre les deux ensembles de fonctions.

Le serveur RAS consigne une erreur dans le journal des événements système si une erreur se produit lors de la tentative de chargement d’une DLL d’administration RAS ou lors de l’appel de l’une des fonctions de la DLL. Cela peut se produire, par exemple, si la DLL spécifiait un nom incorrect pour une fonction exportée, ou si elle n’incluait pas le nom de la fonction dans le fichier. def. L’entrée dans le journal des événements indique la raison de l’échec.

**Windows serveur 2000 et versions ultérieures :** Les dll d’administration RAS qui implémentent cette interface de fonction ne fonctionnent plus. Au lieu de cela, utilisez l’interface de fonction MprAdmin fournie avec les versions les plus récentes de Windows. Pour plus d’informations, consultez les informations de référence sur l' [administration RAS](remote-access-service-administration-reference.md) dans la documentation routage et accès distant.

 

 




