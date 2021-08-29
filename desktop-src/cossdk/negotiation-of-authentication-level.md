---
description: Négociation du niveau d’authentification
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Négociation du niveau d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525a7830b15451d6af54c2422128ba12dcfb56db10a8c2509298ea0ef9821e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070439"
---
# <a name="negotiation-of-authentication-level"></a>Négociation du niveau d’authentification

Le client et le serveur doivent participer à l’authentification, et chaque tiers indique qu’il souhaite effectuer un certain niveau d’authentification. Au début d’un appel, le niveau d’authentification est négocié entre les deux parties, un service approprié est choisi, et l’appel est authentifié et se poursuit (avec un chiffrement possible, selon le niveau d’authentification choisi). Le niveau d’authentification négocié entre le client et le serveur est déterminé comme étant maximal (*préférence du client*, *préférence du serveur*). L’effet de cela signifie que le serveur peut toujours dicter un niveau minimal d’authentification avec lequel il est familiarisé. autrement dit, l’authentification peut être imposée de façon administrative à partir du serveur.

Le client spécifie qu’il souhaite effectuer l’authentification à un certain niveau comme avec n’importe quelle application COM. Le niveau d’authentification du client peut être indiqué comme suit :

-   Par ordinateur client, avec le niveau d’authentification COM à l’échelle de l’ordinateur défini à l’aide de [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) ou de l’outil d’administration Services de composants.
-   Par application cliente administrativement, à l’aide de [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) ou de l’outil d’administration Services de composants si le client doit être une application com+.
-   Par programme client par programme, avec la procédure [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   À tout moment, par programmation, à l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

L’application serveur COM+ spécifie un niveau d’authentification de manière administrative à l’aide de l’outil d’administration Services de composants (ou d’un script d’administration).

La négociation de l’authentification pour un appel se poursuit dans la séquence suivante :

1.  Le niveau d’authentification est choisi comme maximum (*client*, *serveur*).
2.  Négociation du protocole d’authentification.
3.  Le serveur authentifie l’identité du client.
4.  Le cas échéant, le client authentifie l’identité du serveur, en fonction du protocole d’authentification.
5.  Les appels de méthode sont communiqués avec le niveau d’authentification choisi.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
</dt> </dl>

 

 
