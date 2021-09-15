---
description: Les informations d’identification Schannel sont représentées en interne en tant que structures de contexte de certificat \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 les clés privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311373"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 les clés privées

Les informations d’identification Schannel sont représentées en interne en tant que structures de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Schannel localise la [*clé privée*](/windows/desktop/SecGloss/p-gly) associée à un contexte de certificat particulier à l’aide de la propriété de certification de la clé de certificat \_ \_ Prov \_ info \_ prop \_ ID du certificat. À l’aide de cette propriété, Schannel accède à la *clé privée* en appelant la fonction [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) . Pour plus d’informations, consultez [paires de clés publique/privée](/windows/desktop/SecCrypto/public-private-key-pairs).

Chaque information d’identification Schannel contient une référence à une ou plusieurs clés privées, chacune associée à un certificat particulier. Les [*clés privées*](/windows/desktop/SecGloss/p-gly) sont gérées de façon très différente selon que les informations d’identification concernent un client ou un serveur.

## <a name="client-private-keys"></a>Clés privées du client

Les [*clés privées*](/windows/desktop/SecGloss/p-gly) du client sont gérées par le [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) utilisé. Les clés privées du client sont généralement stockées par les fournisseurs de services de type [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) ou Prov \_ RSA \_ signature.

Si l’application cliente effectue l’appel [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) manuellement avant d’appeler [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), le client doit lier le descripteur du CSP au contexte de certificat à l’aide de la \_ propriété CERT Key \_ \_ \_ prop handle prop \_ ID. Si Schannel trouve ce jeu de propriétés, il n’utilise pas la propriété CERTIFICATe de la \_ clé \_ Prov \_ info \_ prop \_ ID.

## <a name="server-private-keys"></a>Clés privées du serveur

Les clés privées du serveur sont stockées par l’un des fournisseurs de services de chiffrement suivants :

-   PROUVER \_ RSA \_ Schannel
-   PROUVER \_ DH \_ Schannel
-   PROUVER le \_ CSP Fortezza

Le choix du fournisseur de services de chiffrement dépend de l' [*algorithme d’échange de clés*](/windows/desktop/SecGloss/k-gly)sélectionné. Les clés privées du serveur doivent être de type au niveau de \_ KeyExchange.

 

 
