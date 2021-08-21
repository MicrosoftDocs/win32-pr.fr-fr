---
description: CredSSP (Credential Security Support Provider Protocol) est un fournisseur de support de sécurité implémenté à l’aide de l’interface SSPI (Security Support Provider Interface).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Fournisseur de support de sécurité des informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4059da0dcc1e6c963ab011ad03415175849191374732f3d1df395914aebe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008737"
---
# <a name="credential-security-support-provider"></a>Fournisseur de support de sécurité des informations d’identification

CredSSP (Credential Security Support Provider Protocol) est un fournisseur de support de sécurité implémenté à l’aide de l’interface[SSPI](sspi.md)(Security Support Provider Interface). CredSSP permet à une application de déléguer les informations d’identification de l’utilisateur du client au serveur cible pour l’authentification distante. CredSSP fournit un canal de [protocole TLS (Transport Layer Security](transport-layer-security-protocol.md) ) chiffré. Le client est authentifié sur le canal chiffré à l’aide du protocole SPNEGO (simple and Protected Negotiate) avec [Microsoft Kerberos](microsoft-kerberos.md) ou [Microsoft NTLM](microsoft-ntlm.md).

> [!Caution]  
> Il ne s’agit pas d’une délégation restreinte. CredSSP transmet les informations d’identification complètes de l’utilisateur au serveur sans aucune contrainte.

 

Pour plus d’informations sur SPNEGO, consultez [Microsoft Negotiate](microsoft-negotiate.md).

Une fois que le client et le serveur sont authentifiés, le client transmet les informations d’identification de l’utilisateur au serveur. Les informations d’identification sont chiffrées doublement sous les clés de session SPNEGO et TLS. CredSSP prend en charge l’ouverture de session par mot de passe, ainsi que l’ouverture de session par carte à puce basée sur [*X. 509*](/windows/desktop/SecGloss/x-gly) et PKINIT.

> [!IMPORTANT]
> CredSSP ne prend pas en charge les clients WOW64.

 

Pour plus d’informations sur CredSSP, consultez les rubriques suivantes.



| Rubrique                                                                         | Description                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [stratégie de groupe CredSSP Paramètres](credssp-group-policy-settings.md)<br/> | La délégation des informations d’identification par CredSSP peut être contrôlée à l’aide des paramètres de stratégie de groupe.<br/> |



 

 

