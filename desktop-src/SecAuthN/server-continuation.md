---
description: En fonction du code de retour d’un appel précédent à AcceptSecurityContext (général), le serveur peut attendre une réponse du client et peut participer à des échanges supplémentaires avec le client.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuation du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06863a0e94fcfe65c7ab695d30be92044fe7341ffa0eb9091c5f1a81acdffc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918288"
---
# <a name="server-continuation"></a>Continuation du serveur

En fonction du code de retour d’un appel précédent à [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), le serveur peut attendre une réponse du client et peut participer à des échanges supplémentaires avec le client. Pour continuer le protocole d’authentification, le serveur répète les appels à **AcceptSecurityContext (général)**.

L’état retourné par [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) est vérifié pour déterminer si le serveur doit attendre des messages supplémentaires du client. Dans la plupart des protocoles d’authentification, il existe un nombre maximal d’échanges même pour l’authentification mutuelle. À l’heure actuelle, les [*protocoles*](../secgloss/k-gly.md) NTLM et Kerberos effectuent une authentification mutuelle avec trois échanges.

 

 
