---
description: Répertorie les packages de sécurité qui peuvent être utilisés avec l’interface SSPI.
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: Utilisation de packages de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df24bba0f910ba74a633e8a43f961cee4fb505db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533669"
---
# <a name="using-security-packages"></a>Utilisation de packages de sécurité

L' [*interface SSPI (Security Support Provider Interface*](../secgloss/s-gly.md) ) peut être utilisée avec les [*packages de sécurité*](../secgloss/s-gly.md)suivants :

-   [Package de sécurité Kerberos](#kerberos-security-package)
-   [Package de sécurité NTLM](#ntlm-security-package)

Les protocoles [*Kerberos*](../secgloss/k-gly.md) et NTLM sont implémentés en tant que packages de sécurité à partir du fournisseur SSP ( [*Security support Provider*](../secgloss/s-gly.md) ) Secur32.dll fourni avec le système d’exploitation. Par défaut, la prise en charge de l’authentification Kerberos et NTLM est chargée par l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) sur un ordinateur au démarrage du système. Dans les domaines Windows Server ou Windows, les deux packages peuvent être utilisés pour authentifier les ouvertures de session réseau et les connexions client/serveur. Celui qui est utilisé dépend des capacités de l’ordinateur de l’autre côté de la connexion. Le protocole Kerberos est toujours préféré, s’il est disponible.

Après l’établissement d’un contexte de sécurité pour un utilisateur interactif, une autre instance du package Kerberos ou NTLM peut être chargée par un processus s’exécutant dans le contexte de sécurité de l’utilisateur afin de prendre en charge l’échange, la signature, la vérification, le chiffrement et le déchiffrement des messages. Toutefois, aucun processus autre que l’autorité LSA n’est autorisé à accéder aux [*clés de session*](../secgloss/s-gly.md) ou aux tickets dans le cache des informations d’identification.

Les services système et les applications de niveau transport accèdent à un fournisseur SSP via SSPI, qui fournit des fonctions pour énumérer les packages de sécurité disponibles sur un système, sélectionner un package et utiliser ce package pour obtenir une connexion authentifiée.

Les méthodes dans SSPI sont des routines génériques que les développeurs peuvent utiliser sans connaître les détails d’un [*protocole de sécurité*](../secgloss/s-gly.md)particulier. Par exemple, lorsqu’une connexion client/serveur est authentifiée :

1.  L’application côté client de la connexion envoie les [*informations d’identification*](../secgloss/c-gly.md) au serveur à l’aide de la fonction SSPI [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
2.  L’application côté serveur de la connexion répond avec la fonction SSPI [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).
3.  Une fois la connexion authentifiée, le LSA sur le serveur utilise les informations du client pour créer un [*jeton d’accès*](../secgloss/a-gly.md).
4.  Le serveur peut ensuite appeler la fonction SSPI [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) pour attacher le jeton d’accès à un thread d’emprunt d’identité pour le service.

## <a name="kerberos-security-package"></a>Package de sécurité Kerberos

Le [*package de sécurité*](../secgloss/s-gly.md) Kerberos est basé sur le [*protocole d’authentification Kerberos*](../secgloss/k-gly.md).

Si le protocole Kerberos est utilisé pour authentifier une connexion client/serveur, [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) génère un message GSSAPI qui comprend un \_ \_ message de demande d’AP AP du client. [**AcceptSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) génère ensuite un message GSSAPI qui comprend un \_ \_ message de rep. AP du serveur.

Pour obtenir des informations générales sur les étapes qui se produisent en arrière-plan dans l’implémentation d’un protocole Kerberos, consultez [Microsoft Kerberos](microsoft-kerberos.md).

Tous les services distribués utilisent SSPI pour accéder au protocole Kerberos. Une liste partielle de la façon dont le protocole Kerberos est utilisé pour l’authentification comprend les éléments suivants :

-   Services spouleur d’impression
-   Accès aux fichiers à distance CIFS/SMB
-   Requêtes [*LDAP*](../secgloss/l-gly.md) adressées au Active Directory
-   Gestion et références du système de fichiers DFS
-   Authentification de l’autorité de sécurité d’hôte à hôte IPsec
-   Demandes de réservation pour la qualité de service du réseau
-   Authentification intranet à Internet Information Services
-   Gestion de serveur distant ou de station de travail à l’aide d’un RPC authentifié
-   [*Demandes de certificat*](../secgloss/c-gly.md) aux services de certificats pour les utilisateurs et les ordinateurs de domaine

## <a name="ntlm-security-package"></a>Package de sécurité NTLM

Le package de sécurité NTLM est basé sur le protocole d’authentification NTLM.

 

 
