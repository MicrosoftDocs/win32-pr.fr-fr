---
description: Le compte LocalService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Compte LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529866"
---
# <a name="localservice-account"></a>Compte LocalService

Le compte LocalService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services. Il possède des privilèges minimum sur l’ordinateur local et présente des informations d’identification anonymes sur le réseau.

Ce compte peut être spécifié dans un appel aux fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Notez que ce compte n’a pas de mot de passe. par conséquent, les informations de mot de passe que vous fournissez dans cet appel sont ignorées. Tandis que le sous-système de sécurité localise ce nom de compte, le SCM ne prend pas en charge les noms localisés. Par conséquent, vous recevrez un nom localisé pour ce compte à partir de la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mais le nom du compte doit être NT Authority \\ LocalService quand vous appelez **CreateService** ou **ChangeServiceConfig**, indépendamment des paramètres régionaux, ou des résultats inattendus peuvent se produire.

Le SID de l’utilisateur est créé à partir de la valeur **\_ \_ \_ RID du service local de sécurité** .

Le compte LocalService possède sa propre sous-clé sous la clé de Registre **HKEY \_ Users** . Par conséquent, la clé de Registre **HKEY \_ Current \_ User** est associée au compte LocalService.

Le compte LocalService dispose des privilèges suivants :

-   **Se \_ \_Nom de ASSIGNPRIMARYTOKEN** (désactivé)
-   **Se \_ \_Nom de l’audit** (désactivé)
-   **Se \_ MODIFIER \_ le \_ nom** de la notification (activé)
-   **Se \_ CRÉER \_ un \_ nom global** (activé)
-   **Se \_ \_Nom d’emprunt d’identité** (activé)
-   **Se \_ AUGMENTER \_ le \_ nom du quota** (désactivé)
-   **Se \_ \_Nom** de l’arrêt (désactivé)
-   **Se \_ Détacher le \_ nom** (désactivé)
-   Tous les privilèges attribués aux utilisateurs et aux utilisateurs authentifiés

Pour plus d’informations, consultez [sécurité des services et droits d’accès](service-security-and-access-rights.md).

 

 
