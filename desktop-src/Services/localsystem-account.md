---
description: Le compte LocalSystem est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: Compte LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233082"
---
# <a name="localsystem-account"></a>Compte LocalSystem

Le compte LocalSystem est un compte local prédéfini utilisé par le gestionnaire de contrôle des services. Ce compte n’est pas reconnu par le sous-système de sécurité. vous ne pouvez donc pas spécifier son nom dans un appel à la fonction [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Il dispose de privilèges étendus sur l’ordinateur local et agit en tant qu’ordinateur sur le réseau. Son jeton comprend les \\ SID système autorité NT et \\ administrateurs BUILTIN. ces comptes ont accès à la plupart des objets système. Le nom du compte dans tous les paramètres régionaux est. \\ LocalSystem. Vous pouvez également utiliser le nom LocalSystem ou *nom_ordinateur* \\ LocalSystem. Ce compte n’a pas de mot de passe. Si vous spécifiez le compte LocalSystem dans un appel à la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) , les informations de mot de passe que vous fournissez sont ignorées.

Un service qui s’exécute dans le contexte du compte LocalSystem hérite du contexte de sécurité du SCM. Le SID de l’utilisateur est créé à partir de la valeur **\_ \_ \_ RID du système local de sécurité** . Le compte n’est associé à aucun compte d’utilisateur connecté. Cela a plusieurs conséquences :

-   La clé de Registre **HKEY \_ Current \_ User** est associée à l’utilisateur par défaut, et non à l’utilisateur actuel. Pour accéder au profil d’un autre utilisateur, emprunter l’identité de l’utilisateur, puis accéder à **HKEY \_ Current \_ User**.
-   Le service peut ouvrir la clé de Registre **HKEY \_ local \_ machine \\ Security**.
-   Le service présente les informations d’identification de l’ordinateur aux serveurs distants.
-   Si le service ouvre une fenêtre de commande et exécute un fichier de commandes, l’utilisateur peut appuyer sur CTRL + C pour mettre fin au fichier de commandes et accéder à une fenêtre de commande avec des autorisations LocalSystem.

Le compte LocalSystem dispose des privilèges suivants :

-   **se \_ \_Nom de ASSIGNPRIMARYTOKEN** (désactivé)
-   **se \_ \_Nom de l’audit** (activé)
-   **se \_ \_Nom** de la sauvegarde (désactivé)
-   **se \_ MODIFIER \_ le \_ nom** de la notification (activé)
-   **se \_ CRÉER \_ un \_ nom global** (activé)
-   **se \_ CRÉER \_ un \_ nom de fichier d’échange** (activé)
-   **se \_ CRÉER \_ un \_ nom permanent** (activé)
-   **se \_ CRÉER \_ un \_ nom de jeton** (désactivé)
-   **se \_ \_Nom du débogage** (activé)
-   **se \_ \_Nom d’emprunt d’identité** (activé)
-   **se \_ Nom de la \_ \_ priorité \_ de base Inc** (activé)
-   **se \_ AUGMENTER \_ le \_ nom du quota** (désactivé)
-   **se \_ CHARGER \_ le \_ nom du pilote** (désactivé)
-   **se \_ VERROUILLER \_ le \_ nom de mémoire** (activé)
-   **se \_ GÉRER \_ le \_ nom du volume** (désactivé)
-   **se \_ \_Nom de \_ processus \_ unique Prof** (activé)
-   **se \_ \_Nom** de la restauration (désactivé)
-   **se \_ \_Nom de sécurité** (désactivé)
-   **se \_ \_Nom** de l’arrêt (désactivé)
-   **se \_ \_ \_ Nom de l’environnement système** (désactivé)
-   **se \_ \_Nom SYSTEMTIME** (désactivé)
-   **se \_ PRENDRE \_ le \_ nom** de la propriété (désactivé)
-   **se \_ \_Nom TCB** (activé)
-   **se \_ Détacher le \_ nom** (désactivé)

La plupart des services n’ont pas besoin d’un tel niveau de privilège élevé. Si votre service n’a pas besoin de ces privilèges et qu’il ne s’agit pas d’un service interactif, envisagez d’utiliser le [compte LocalService](localservice-account.md) ou [NetworkService](networkservice-account.md). Pour plus d’informations, consultez [sécurité des services et droits d’accès](service-security-and-access-rights.md).

 

 
