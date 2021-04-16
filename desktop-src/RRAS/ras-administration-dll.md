---
title: À propos des dll d’administration RAS
description: La DLL d’administration RAS exporte les fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter.
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- Administration RAS RRAS, DLL d’administration RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb170e8cfa331ab9591aa509772c6f6a743fa49
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104507743"
---
# <a name="about-ras-administration-dlls"></a>À propos des dll d’administration RAS

La DLL d’administration RAS exporte les fonctions que le serveur RAS appelle chaque fois qu’un utilisateur tente de se connecter ou de se déconnecter. Voici quelques-unes des utilisations possibles d’une DLL d’administration RAS :

-   Décidez s’il faut autoriser un utilisateur à se connecter au serveur. La DLL d’administration peut fournir une vérification de sécurité en plus de l’authentification utilisateur RAS standard.
-   Enregistrez l’heure à laquelle chaque utilisateur se connecte et se déconnecte du serveur. Cela peut être utile à des fins de facturation ou d’audit.
-   Attribuez une adresse IP à chaque utilisateur. Cela est utile pour la sécurité, car cette fonctionnalité est utilisée pour mapper la connexion d’un utilisateur à un ordinateur spécifique.

L’emplacement de la DLL d’administration RAS est spécifié dans le registre ; consultez [configuration du registre des dll d’administration RAS](ras-administration-dll-registry-setup.md).

RAS prend en charge plusieurs DLL d’administration. Le registre prend en charge plusieurs emplacements de DLL. RAS appelle les fonctions dans les dll dans l’ordre dans lequel les dll sont répertoriées dans le registre ; consultez [configuration du registre des dll d’administration RAS](ras-administration-dll-registry-setup.md).

**Serveur Windows 2000 :** RAS ne prend pas en charge plusieurs dll.

Une DLL d’administration RAS doit implémenter et exporter toutes les fonctions suivantes :

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

En outre, la DLL d’administration RAS doit implémenter et exporter

[**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) et

[**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

ou

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) et

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

Si toutes les fonctions requises ne sont pas implémentées, RAS ne peut pas démarrer.

**Serveur Windows 2000 :** Une DLL d’administration doit implémenter les fonctions [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) et [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) . Si la DLL implémente l’une de ces fonctions, elle doit également implémenter l’autre.

RAS appelle la fonction [**MprAdminInitializeDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) lorsque le service Routage et accès distant démarre pour la première fois. La fonction **MprAdminInitializeDll** permet à la dll d’administration d’effectuer toute initialisation nécessaire. De même, RAS appelle le service [**MprAdminTerminateDll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) lorsque le service de routage et d’accès distant s’arrête. Cette fonction permet à la DLL d’administration d’effectuer tout nettoyage nécessaire avant de quitter.

Les fonctions [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) et [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) permettent à la dll d’auditer les connexions utilisateur au serveur. Un serveur RAS appelle la fonction **MprAdminAcceptNewConnection** chaque fois qu’un utilisateur tente de se connecter. Cette fonction permet d’empêcher l’utilisateur de se connecter. La fonction **MprAdminAcceptNewConnection** peut également générer des entrées de journal pour la facturation ou l’audit. Lorsque l’utilisateur se déconnecte, le serveur RAS appelle la fonction **MprAdminConnectionHangupNotification** , qui peut consigner l’heure à laquelle l’utilisateur s’est déconnecté.

Les fonctions [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) et [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2) sont similaires à **MprAdminAcceptNewConnection** et [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification). Toutefois, lorsque RAS appelle les fonctions **MprAdminAcceptNewConnection2** et **MprAdminConnectionHangupNotification2** , Ras passe dans un paramètre supplémentaire de type [**RAS \_ Connection \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2).

RAS prend en charge plusieurs DLL d’administration. L’utilisateur à accès à distance est autorisé à se connecter uniquement si l’implémentation de la fonction [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) ou [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) dans chacune des dll accepte la connexion. En d’autres termes, chaque DLL doit accepter la connexion afin que l’utilisateur soit autorisé à se connecter.

Il est possible qu’une seule connexion RAS utilise plusieurs liens lors de la connexion à un serveur RAS. Les fonctions [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) et [**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification) permettent à la dll d’administration de gérer des liens individuels dans une connexion. RAS appelle **MprAdminAcceptNewLink** chaque fois qu’un nouveau lien est établi pour une connexion. Étant donné que toutes les connexions impliquent au moins un lien, RAS appelle toujours **MprAdminAcceptNewLink** une fois immédiatement après le retour de [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) ou [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) , à condition que [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) ou [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) ait accepté la connexion. RAS appelle **MprAdminLinkHangupNotification** chaque fois qu’un lien pour une connexion est arrêté.

Étant donné que RAS prend en charge plusieurs DLL d’administration, l’utilisateur à accès à distance est autorisé à se connecter uniquement si l’implémentation de la fonction [**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) dans chacune des dll accepte la connexion. En d’autres termes, chaque DLL doit accepter le lien pour pouvoir établir le lien.

Une fois qu’un utilisateur a été authentifié par le serveur RAS, il appelle la fonction [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) pour obtenir une adresse IP pour le client distant. Cette fonction fournit un autre modèle pour le mappage d’une adresse IP à un utilisateur d’accès à distance. Si **MprAdminGetIpAddressForUser** n’est pas implémenté, un serveur RAS associe l’utilisateur distant à une adresse IP qui est sélectionnée à partir d’un pool statique d’adresses IP, ou celle sélectionnée par un serveur DHCP (Dynamic Host Configuration Protocol). La fonction **MprAdminGetIpAddressForUser** permet à la dll de remplacer cette adresse IP par défaut et de spécifier une adresse IP spécifique pour chaque utilisateur. La fonction **MprAdminGetIpAddressForUser** peut définir un indicateur qui force RAS à appeler la fonction [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) lorsque l’utilisateur se déconnecte. La DLL peut ensuite utiliser **MprAdminReleaseIpAddress** pour mettre à jour son mappage utilisateur-adresse IP.

RAS prend en charge plusieurs DLL d’administration, mais il appelle uniquement les fonctions [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) et [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) dans la première dll qui les implémente et les exporte. RAS ignore les implémentations de ces fonctions dans les autres dll. RAS vérifie les dll de ces fonctions dans l’ordre dans lequel elles sont répertoriées dans le [Registre](ras-administration-dll-registry-setup.md).

RAS sérialise les appels dans la DLL d’administration. Un appel à l’une des fonctions de la DLL pour un client RAS donné ne devance pas un appel à cette fonction pour un autre client RAS. RAS n’appelle pas la fonction pour l’autre client tant que l’appel initial n’est pas terminé. En outre, la sérialisation s’étend à certains groupes de fonctions. Les fonctions d’adresse IP sont sérialisées en tant que groupe ; un appel dans [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) ou [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) bloque les appels dans les deux fonctions jusqu’à ce que l’appel initial soit retourné. [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) et [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) sont également sérialisés en tant que groupe.

RAS exécute les fonctions qui attribuent des adresses IP en un seul processus. les fonctions pour les notifications de connexion et de déconnexion sont exécutées dans un autre processus. Par conséquent, la DLL ne dépend pas des données partagées entre ces deux ensembles de fonctions.

N’appelez aucune des fonctions d' [administration RAS](ras-administration-functions.md) ou des [fonctions d’administration de l’utilisateur RAS](ras-user-administration-functions.md) à partir d’une fonction de légende. Les appels à ces fonctions ne sont pas retournés lorsqu’ils sont effectués à partir d’une fonction de légende.

Le serveur RAS consigne une erreur dans le journal des événements système si une erreur se produit lors de la tentative de chargement d’une DLL d’administration RAS ou lors de l’appel de l’une des fonctions de la DLL. Cela peut se produire, par exemple, si la DLL spécifiait un nom incorrect pour une fonction exportée, ou si elle n’incluait pas le nom de la fonction dans le fichier DEF. L’entrée dans le journal des événements indique la raison de l’échec.

**Windows 2000/NT :** Plusieurs DLL d’administration ne sont pas prises en charge.

 

 




