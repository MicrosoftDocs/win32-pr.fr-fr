---
description: Mappage des certificats
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mappage des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f671afa6278da49427d0f7b49f78895198333e24d135383207b359846216638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921838"
---
# <a name="mapping-certificates"></a>Mappage des certificats

> [!Note]  
> Les informations contenues dans cette rubrique ne sont valides que pour les serveurs qui requièrent l’authentification du client.

 

Lorsqu’une application serveur requiert l’authentification du client, Schannel tente automatiquement de mapper le certificat fourni par le client à un compte d’utilisateur.

Une fois [*le contexte de sécurité*](../secgloss/s-gly.md) établi, l’application serveur peut utiliser la fonction [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) pour obtenir un [*jeton d’accès*](../secgloss/a-gly.md) pour le compte d’utilisateur auquel le [*certificat client*](../secgloss/c-gly.md) a été mappé. En outre, le serveur peut utiliser la fonction [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) pour emprunter l’identité du client.

Pour plus d’informations sur l’authentification, consultez [exécution de l’authentification à l’aide de Schannel](performing-authentication-using-schannel.md).

 

 
