---
description: Comme pour le client, le serveur acquiert également un handle d’informations d’identification pour être prêt à répondre à une demande d’authentification entrante à partir du client.
ms.assetid: 2a0aeadf-e099-4264-8522-e498f437bf75
title: Initialisation du contexte de serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d4a81c8033dc6b5dda8baca9ee7dfcc87d2b14c1cd139ff4a7f8eda99603f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918328"
---
# <a name="server-context-initialization"></a>Initialisation du contexte de serveur

Comme pour le client, le serveur acquiert également un handle [*d’informations d’identification*](../secgloss/c-gly.md) pour être prêt à répondre à une demande d’authentification entrante à partir du client. Les informations d’identification du serveur sont utilisées pour authentifier le serveur auprès du client dans les [*protocoles de sécurité*](../secgloss/s-gly.md) qui prennent en charge l’authentification du serveur ou l’authentification mutuelle. Le serveur obtient un descripteur des informations d’identification définies par le compte de service utilisé pour démarrer le serveur. Pour ce faire, il appelle [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).

Le serveur peut acquérir son handle d’informations d’identification, puis passer à un état d’écoute, ou il peut attendre dans un état d’écoute jusqu’à ce qu’une demande de connexion arrive, puis acquérir un handle d’informations d’identification entrantes. Pour plus d’informations sur les fonctions d’informations d’identification, consultez [gestion des informations d’identification](authentication-functions.md).

Lorsque le serveur reçoit un message de demande de connexion d’un client, il crée un [*contexte de sécurité*](../secgloss/s-gly.md) local pour le client à l’aide de [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext). Le serveur utilise ce contexte de sécurité local pour exécuter les demandes ultérieures par le même client. Pour plus d’informations sur les fonctions de contexte, consultez [gestion du contexte](authentication-functions.md).

Le serveur vérifie le descripteur d’état de retour et de mémoire tampon de sortie pour s’assurer qu’il n’y a pas d’erreurs jusqu’à présent et peut rejeter la demande de connexion s’il y a des erreurs. Si la mémoire tampon de sortie est retournée par [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), cette mémoire tampon est regroupée dans un message de réponse au client.

Toute mémoire tampon de sortie provenant de [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) doit être renvoyée au client. En outre, si l’état de retour nécessite que le protocole se poursuive (SEC \_ i continue required \_ \_ ou s \_ i \_ Completed \_ and \_ continue), un autre échange de messages avec le client est requis.

Pour les jambes supplémentaires, le serveur attend que le client réponde avec un autre message. Cette attente peut être dépassée afin d’éviter une attaque par déni de service dans laquelle un client ne répond jamais intentionnellement, provoquant un thread de serveur et, de temps en temps, tous les threads de serveur, pour ne plus répondre.

 

 
