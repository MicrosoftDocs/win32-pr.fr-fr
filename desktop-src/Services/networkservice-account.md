---
description: Le compte NetworkService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Compte NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233075"
---
# <a name="networkservice-account"></a>Compte NetworkService

Le compte NetworkService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services. Ce compte n’est pas reconnu par le sous-système de sécurité. vous ne pouvez donc pas spécifier son nom dans un appel à la fonction [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Il possède des privilèges minimum sur l’ordinateur local et agit en tant qu’ordinateur sur le réseau.

Ce compte peut être spécifié dans un appel aux fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Notez que ce compte n’a pas de mot de passe. par conséquent, les informations de mot de passe que vous fournissez dans cet appel sont ignorées. Tandis que le sous-système de sécurité localise ce nom de compte, le SCM ne prend pas en charge les noms localisés. Par conséquent, vous recevrez un nom localisé pour ce compte à partir de la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mais le nom du compte doit être NT Authority \\ NetworkService quand vous appelez **CreateService** ou **ChangeServiceConfig**, indépendamment des paramètres régionaux, ou des résultats inattendus peuvent se produire.

Un service qui s’exécute dans le contexte du compte NetworkService présente les informations d’identification de l’ordinateur aux serveurs distants. Par défaut, le jeton distant contient des SID pour les groupes tout le monde et utilisateurs authentifiés. Le SID de l’utilisateur est créé à partir de la valeur **\_ \_ \_ RID du service réseau de sécurité** .

Le compte NetworkService possède sa propre sous-clé sous la clé de Registre **HKEY \_ Users** . Par conséquent, la clé de Registre **HKEY \_ Current \_ User** est associée au compte NetworkService.

Le compte NetworkService dispose des privilèges suivants :

-   **se \_ \_Nom de ASSIGNPRIMARYTOKEN** (désactivé)
-   **se \_ \_Nom de l’audit** (désactivé)
-   **se \_ MODIFIER \_ le \_ nom** de la notification (activé)
-   **se \_ CRÉER \_ un \_ nom global** (activé)
-   **se \_ \_Nom d’emprunt d’identité** (activé)
-   **se \_ AUGMENTER \_ le \_ nom du quota** (désactivé)
-   **se \_ \_Nom** de l’arrêt (désactivé)
-   **se \_ Détacher le \_ nom** (désactivé)
-   Tous les privilèges attribués aux utilisateurs et aux utilisateurs authentifiés

Pour plus d’informations, consultez [sécurité des services et droits d’accès](service-security-and-access-rights.md).

 

 
