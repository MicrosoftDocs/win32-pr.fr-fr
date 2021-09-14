---
title: Définition des autorisations sur les répertoires virtuels
description: Pour des raisons de sécurité, Service de transfert intelligent en arrière-plan (BITS) ne télécharge pas les fichiers vers un répertoire virtuel pour lequel les autorisations de script et d’exécution sont activées.
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999568"
---
# <a name="setting-permissions-on-virtual-directories"></a>Définition des autorisations sur les répertoires virtuels

Pour des raisons de sécurité, Service de transfert intelligent en arrière-plan (BITS) ne télécharge pas les fichiers vers un répertoire virtuel pour lequel les autorisations de script et d’exécution sont activées. Si vous chargez un fichier dans un répertoire virtuel pour lequel ces autorisations sont activées, le travail échoue avec un code d’erreur d' \_ exécution du serveur BG E \_ \_ \_ activé.

Le service BITS ne nécessite pas l’activation de l’écriture dans le répertoire virtuel. il est donc recommandé de désactiver l’accès en écriture au répertoire virtuel.

L’utilisateur authentifié (ou l’utilisateur anonyme d’IIS pour l’authentification anonyme) doit disposer d’autorisations de modification sur le répertoire physique auquel le répertoire virtuel est mappé ; l’octroi d’autorisations en écriture ne suffit pas.

## <a name="specifying-permissions-for-notifications"></a>Spécification des autorisations pour les notifications

Le schéma d’authentification que vous spécifiez pour le répertoire virtuel et l’URL de notification (voir la propriété [BITSServerNotificationURL](bits-iis-extension-properties.md) ) doit être compatible. Le service BITS utilise le schéma d’authentification spécifié pour que le répertoire virtuel accède à l’URL de notification. Le travail de chargement échoue si le service BITS ne peut pas accéder à l’URL de notification en raison d’un échec d’authentification.

Si le type de notification (voir la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) ) est [par référence](using-bits-notification-request-response-headers.md), l’application doit s’assurer que l’utilisateur a accès au fichier référencé (consultez l’en-tête [bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) ). BITS définit les listes de contrôle d’accès sur le fichier référencé sur celles du répertoire physique auquel le répertoire virtuel est mappé.

> [!Note]  
> L’application notifiée doit être en mesure de mapper et d’accéder au fichier distant même si l’URL de notification est desservie par un serveur Web situé sur un autre ordinateur que le répertoire de chargement physique. L’en-tête [bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) contient toujours une spécification de chemin d’accès relative à l’ordinateur hébergeant le composant extensions bits. Une application s’exécutant sur un autre ordinateur peut avoir besoin de convertir le chemin en chemin UNC avant d’y accéder.

 

BITS prend en charge de nombreuses combinaisons de schémas d’authentification. Toutefois, vous devez utiliser le schéma d’authentification suivant pour le répertoire virtuel et l’URL de notification correspondante.

-   Pour prendre en charge les notifications de référence, le répertoire virtuel doit être configuré pour utiliser l’authentification NTLM (Negotiate) si le répertoire de chargement physique (le répertoire vers lequel pointe le répertoire virtuel) utilise un schéma d’authentification autre que anonyme. Si le répertoire de chargement physique autorise les requêtes anonymes (aucune authentification), le répertoire virtuel doit activer l’authentification anonyme (aucune authentification).

    Les listes de contrôle d’accès du répertoire de chargement physique doivent être définies de sorte que l’utilisateur authentifié puisse lire les fichiers du répertoire vers lequel pointe l’URL de notification. BITS utilise les listes de contrôle d’accès du répertoire de chargement physique pour définir les listes de contrôle d’accès du fichier de téléchargement temporaire (l’en-tête [bits-Request-DataFile-Name](notification-protocol-for-server-applications.md) contient le chemin d’accès au fichier temporaire).

-   Étant donné que les notifications [par valeur](using-bits-notification-request-response-headers.md) ne nécessitent pas que l’application notifiée accède à un fichier temporaire qui contient le contenu de téléchargement, le schéma d’authentification peut être anonyme ou négocier (NTLM). La seule exigence est que l’utilisateur authentifié pour le répertoire virtuel doit également être autorisé à accéder à l’URL de notification.

## <a name="specifying-permissions-for-remote-shares"></a>Spécification des autorisations pour les partages distants

Un répertoire virtuel peut pointer vers un lecteur mappé sur un autre ordinateur ou un partage réseau. S’il pointe vers un lecteur réseau mappé, les informations d’identification utilisées pour mapper le lecteur doivent disposer d’un contrôle total sur le partage distant.

si le répertoire virtuel pointe vers un partage réseau, le service BITS utilise le Connecter du répertoire virtuel **en tant qu'** informations d’identification de l’utilisateur pour accéder au partage distant. pour accéder à un partage distant, le **Connecter compte en tant** que compte doit avoir des privilèges, comme décrit dans la documentation de la fonction [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) . BITS se connecte à l’aide des types d’ouverture de session \_ \_ interactive LOGON32 batch ou LOGON32 \_ Logon \_ . le **Connecter en tant que** compte d’utilisateur a besoin d’autorisations Full-Access sur le partage distant ; l’octroi d’autorisations en écriture ne suffit pas.

lorsque le répertoire de chargement physique est mappé à un partage réseau, l’identité de l’appelant demandant l’URL de notification est soit le **Connecter en tant qu'** utilisateur, soit l’utilisateur authentifié du répertoire de chargement physique (uniquement disponible dans IIS 6,0 et versions ultérieures, lorsque la case à cocher **utilise toujours les informations d’identification de l’utilisateur authentifié lors de la validation de l’accès à la ressource réseau** est sélectionnée dans la boîte de dialogue **Connecter en tant que** ).

 

 