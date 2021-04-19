---
description: En fonction du code de retour d’un appel précédent à AcceptSecurityContext (général), le serveur peut attendre une réponse du client et peut participer à des échanges supplémentaires avec le client.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuation du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534245"
---
# <a name="server-continuation"></a>Continuation du serveur

En fonction du code de retour d’un appel précédent à [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), le serveur peut attendre une réponse du client et peut participer à des échanges supplémentaires avec le client. Pour continuer le protocole d’authentification, le serveur répète les appels à **AcceptSecurityContext (général)**.

L’état retourné par [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) est vérifié pour déterminer si le serveur doit attendre des messages supplémentaires du client. Dans la plupart des protocoles d’authentification, il existe un nombre maximal d’échanges même pour l’authentification mutuelle. À l’heure actuelle, les [*protocoles*](../secgloss/k-gly.md) NTLM et Kerberos effectuent une authentification mutuelle avec trois échanges.

 

 
