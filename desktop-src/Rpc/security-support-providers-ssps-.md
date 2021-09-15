---
title: Fournisseurs de support de sécurité (SSP)
description: à partir de Windows 2000, RPC prend en charge un large éventail de fournisseurs et de packages de sécurité.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413547"
---
# <a name="security-support-providers-ssps"></a>Fournisseurs de support de sécurité (SSP)

à partir de Windows 2000, RPC prend en charge un large éventail de fournisseurs et de packages de sécurité. En voici quelques-uns :

-   **Package de sécurité du protocole Kerberos.** Le protocole Kerberos v5 est un package de sécurité standard. Il utilise les noms principaux de fullsic.
-   **SSP SCHANNEL.** Ce fournisseur de services partagés implémente le package de sécurité du fournisseur de protocole unifié Microsoft, qui unifie les protocoles SSL, les technologies de communication privée (PCT) et la sécurité au niveau du transport (TLS) dans un seul package de sécurité. Il reconnaît les noms principaux msstd et fullsic.
-   **Package de sécurité NTLM.** il s’agissait du package de sécurité principal pour les réseaux NTLM antérieur à Windows 2000.

En outre, Microsoft RPC fournit un *Pseudo-SSP* qui permet aux applications de négocier entre l’utilisation de SSP réels. Ce Pseudo-SSP, appelé simple SSP Snego (simple GSS-API Negotiation Mechanism), ne fournit pas de fonctionnalités d’authentification réelles. Sa seule utilisation est d’aider les applications à sélectionner un fournisseur de services partagés réel. Actuellement, les programmes client et serveur peuvent utiliser le SSP Snego pour négocier entre l’utilisation du package de sécurité NTLM et du package de sécurité du protocole Kerberos. Pour plus d’informations sur la sélection des fournisseurs de services partagés, consultez [Authentication-Service constants](authentication-service-constants.md).

Tous les SSP fournis par Microsoft, à l’exception de SCHANNEL, reconnaissent les informations d’identification d’authentification sous la forme fournie par la seconde structure d’identité d’authentification [**\_ winnt \_ \_**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . Pour plus d’informations, consultez [informations d’identification de l’authentification du client](client-authentication-credentials.md). Pour plus d’informations sur l’utilisation de SSP spécifiques, consultez [fonctions SSPI](/windows/desktop/SecMgmt/management-functions) et [utilisation du fournisseur de sécurité Schannel](/windows/desktop/SecAuthN/secure-channel) dans la documentation sur la sécurité du kit de développement logiciel (SDK) de la plateforme.

 

 