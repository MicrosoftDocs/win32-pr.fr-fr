---
description: Comment créer une connexion sécurisée à l’aide de Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Création d’une connexion sécurisée à l’aide de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757293"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Création d’une connexion sécurisée à l’aide de Schannel

Le [*package de sécurité*](/windows/desktop/SecGloss/s-gly) Schannel donne accès à quatre [*protocoles de sécurité*](/windows/desktop/SecGloss/s-gly):

-   [Transport Layer Security (TLS 1,2)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1,1)](transport-layer-security-protocol.md)
-   [Transport Layer Security (TLS 1,0)](transport-layer-security-protocol.md)
-   [SSL (Secure Sockets Layer) (SSL 3,0)](secure-sockets-layer-protocol.md)
-   [SSL (Secure Sockets Layer) (SSL 2,0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Les protocoles PCT et SSL 2,0 ont été remplacés par le protocole TLS et ne doivent pas être utilisés pour un nouveau développement.

 

**Pour configurer une connexion sécurisée entre un client et un serveur**

1.  Obtenir des informations d’identification Schannel (en[obtenant des informations d’identification Schannel](obtaining-schannel-credentials.md)).
2.  Créer un contexte de sécurité Schannel ([création d’un contexte de sécurité Schannel](creating-an-schannel-security-context.md)).

Une fois la connexion établie, vous pouvez récupérer des informations sur ses attributs. Pour plus d’informations, consultez [obtention d’informations sur les connexions Schannel](getting-information-about-schannel-connections.md).

Si, après avoir établi une connexion, les exigences de sécurité de votre application changent ou la connexion est perdue, vous pouvez renégocier la connexion. Pour plus d’informations, consultez [renégociation d’une connexion Schannel](renegotiating-an-schannel-connection.md).

Une fois que vous avez fini d’utiliser une connexion Schannel, vous devez effectuer le nettoyage nécessaire. Pour plus d’informations, consultez [arrêt d’une connexion Schannel](shutting-down-an-schannel-connection.md).

Pour plus d’informations sur les exemples fournis avec le kit de développement logiciel (SDK) de plateforme qui illustrent le [*package de sécurité*](/windows/desktop/SecGloss/s-gly)Schannel, consultez les exemples de SDK à l’aide de Schannel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification des chiffrements Schannel et des forces de chiffrement](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
