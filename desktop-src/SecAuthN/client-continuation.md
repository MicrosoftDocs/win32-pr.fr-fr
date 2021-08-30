---
description: Certains protocoles nécessitent plusieurs messages d’authentification.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuation du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007a6fbc3d9fd887b041bf23267ddb804665d733e057c717041ae02b3bb53513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883449"
---
# <a name="client-continuation"></a>Continuation du client

Certains protocoles nécessitent plusieurs messages d’authentification. Dans ce cas, le client analyse la réponse du serveur et appelle [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) à nouveau à l’aide de l’état continue de l’appel précédent. Le client vérifie l’état renvoyé à partir de cet appel et peut être amené à continuer pour les jambes supplémentaires. Elle utilise les informations de *pOutput* pour construire un message et l’envoyer au serveur.

 

 
