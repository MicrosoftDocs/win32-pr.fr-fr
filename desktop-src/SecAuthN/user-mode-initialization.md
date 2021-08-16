---
description: Les applications distribuées (client/serveur) utilisent des packages de sécurité pour obtenir des connexions authentifiées et échanger des messages.
ms.assetid: 8f28177f-335a-4fa2-bf66-2ec1698bebec
title: Initialisation du mode utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be7c4c00937473e2ecc3d6b01bb7c59a2842085a133f381b5a8a10bd9b215f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915581"
---
# <a name="user-mode-initialization"></a>Initialisation du mode utilisateur

Les applications distribuées (client/serveur) utilisent des [*packages de sécurité*](../secgloss/s-gly.md) pour obtenir des connexions authentifiées et échanger des messages. L’application appelle les fonctions SSPI (Security Support Provider Interface) qui sont mappées aux [fonctions implémentées par le fournisseur SSP/APS](authentication-functions.md), ainsi que les [fonctions implémentées par SSP/APS en mode utilisateur](authentication-functions.md). Ce mappage est effectué par la DLL du fournisseur de sécurité (Secur32.dll ou Security.dll), qui peut être chargée dynamiquement dans les processus du client et du serveur. La DLL peut également être liée de manière statique à l’aide de secur32. lib. la DLL et la bibliothèque sont fournies avec le kit de développement logiciel (SDK) Microsoft Windows.

Le chargement du package de sécurité dans le processus du client ou du serveur est géré par le système, si la DLL SSP/AP qui contient le package de sécurité est correctement inscrite.

Le serveur commence le processus d’obtention d’une connexion sécurisée avec un client en surveillant un port, en attendant qu’un client envoie un message. Le client commence le processus d’obtention d’une connexion sécurisée au serveur en appelant la fonction SSPI [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Cette fonction est mappée à la fonction [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) du package de sécurité personnalisé. **SpInitLsaModeContext** retourne un jeton au client, qui le transfère au serveur.

Lors de la réception du jeton du client, le serveur appelle la fonction SSPI [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), qui est distribuée à la fonction [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) du package de sécurité. Si la fonction **SpAcceptLsaModeContext** réussit et qu’aucun autre traitement n’est nécessaire pour établir le contexte de sécurité, la fonction doit retourner l’état \_ Success à l’appelant. Si un traitement supplémentaire est requis, la fonction doit retourner SEC \_ je \_ continue \_ nécessaire et retourner un jeton au serveur. Le serveur transfère le jeton au client, qui appelle [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

Ce cycle appelant peut être répété aussi souvent que nécessaire, jusqu’à ce qu’une connexion authentifiée soit établie ou échoue. Au cours de ce processus, si la fonction [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) ou [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) réussit et qu’aucun autre traitement n’est nécessaire pour établir le [*contexte de sécurité*](../secgloss/s-gly.md), la fonction doit retourner l’état \_ Success à l’appelant. Si un traitement supplémentaire est requis, la fonction doit retourner SEC \_ je \_ continue \_ nécessaire et retourner un jeton à l’appelant, qui est chargé de le transférer.

Le protocole implémenté par le package de sécurité détermine le nombre de fois où ce cycle est répété. Par exemple, dans les packages de sécurité qui prennent en charge l’authentification mutuelle à trois jambes, la séquence d’appel est la suivante :

1.  Le client obtient un jeton en appelant [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)et l’envoie au serveur. Le serveur appelle [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) la première fois et récupère un jeton de réponse qu’il envoie au client.
2.  Le client utilise le jeton reçu du serveur lors d’un deuxième appel à [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)et récupère un jeton final. Le client envoie ce jeton au serveur.
3.  Le serveur reçoit le jeton généré dans Leg 2 qu’il utilise dans l’appel final à [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

Lorsque les fonctions [**SpAcceptLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spacceptlsamodecontextfn) et [**SpInitLsaModeContext**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitlsamodecontextfn) réussissent et qu’aucun traitement supplémentaire n’est nécessaire pour établir le contexte de sécurité, les fonctions doivent retourner l’état \_ Success à l’appelant. En outre, si le package de sécurité personnalisé prend en charge les [fonctions implémentées par SSP/APS en mode utilisateur](authentication-functions.md), **SpAcceptLsaModeContext** et **SpInitLsaModeContext** doivent retourner la **valeur true** par le biais du paramètre *MappedContext* . La valeur *MappedContext* n’est pas renvoyée à l’application ; elle est interceptée par l’autorité LSA.

Quand *MappedContext* a la **valeur true**, l’autorité LSA appelle la fonction [**SpUsermodeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spusermodeinitializefn) de la dll SSP/AP. Cette fonction fournit des tableaux de pointeurs vers les fonctions en mode utilisateur implémentées par chaque package de sécurité. La fonction [**SpInstanceInit**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinstanceinitfn) de chaque package est appelée, à l’aide des tables de fonctions retournées par **SpUsermodeInitialize**. **SpInstanceInit** reçoit une table de pointeurs vers les [fonctions LSA appelées par SSP/APS en mode utilisateur](authentication-functions.md).

 

 
