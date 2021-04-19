---
description: Pour modifier les attributs d’une connexion, tels que la suite de chiffrement ou l’authentification du client, vous pouvez demander une &\# 0034 ; rétablir&\# 0034 ; ou la renégociation de la connexion.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Renégociation d’une connexion Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544833"
---
# <a name="renegotiating-an-schannel-connection"></a>Renégociation d’une connexion Schannel

Pour modifier les attributs d’une connexion, tels que la suite de chiffrement ou l’authentification du client, vous pouvez demander un « rétablissement » ou une renégociation de la connexion.

Si les attributs que vous souhaitez modifier sont contrôlés par des informations d’identification, vous devez obtenir de nouvelles informations d’identification avant de renégocier la connexion. Pour plus d’informations, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md).

Pour demander une restauration par progression à partir d’une application cliente, appelez la fonction [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) . Les applications serveur appellent la fonction [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) . Définissez les paramètres de la façon suivante :

-   Spécifiez le [*contexte de sécurité*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) existant dans le paramètre *phContext* .
-   (Clients uniquement) Spécifiez le même nom de serveur (dans le paramètre *pszTargetName* ) comme spécifié lors de l’établissement du contexte.
-   Spécifiez de nouvelles informations d’identification à l’aide du paramètre *phCredential* , le cas échéant.
-   Si vous souhaitez modifier les attributs de contexte qui ne sont pas liés aux informations d’identification, spécifiez ces attributs à l’aide du paramètre *fContextReq* .

Après avoir appelé la fonction appropriée, votre application doit envoyer les résultats au client et continuer à traiter les messages entrants à l’aide de la fonction [**DecryptMessage (SChannel)**](decryptmessage--schannel.md) .

La fonction [**DecryptMessage (SChannel)**](decryptmessage--schannel.md) renvoie les secondes \_ que je \_ renégocie lorsque Schannel est prêt pour que votre application continue. Lorsque vous recevez le \_ \_ Code de retour sec I renégocier, votre application doit appeler [**AcceptSecurityContext (SChannel)**](acceptsecuritycontext--schannel.md) (Servers) ou [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) (clients) et transmettre le contenu de SECBUFFER_EXTRA retourné à partir de DecryptMessage dans le SECBUFFER_TOKEN. Après que cet appel a retourné une valeur, procédez comme si votre application était en train de créer une nouvelle connexion.

 

 
