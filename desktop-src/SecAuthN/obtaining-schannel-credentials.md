---
description: Les informations d’identification sont requises par le processus d’authentification Schannel. le client et le serveur doivent obtenir des informations d’identification valides pour établir un contexte de sécurité pour l’échange de messages. Pour obtenir un exemple qui illustre cette procédure, consultez obtention d’informations d’identification.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtention des informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123345"
---
# <a name="obtaining-schannel-credentials"></a>Obtention des informations d’identification Schannel

Les informations d’identification sont requises par le processus d’authentification Schannel. le client et le serveur doivent obtenir des informations d’identification valides pour établir un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages. Pour obtenir un exemple qui illustre cette procédure, consultez [obtention d’informations d’identification](getting-a-certificate-for-schannel.md).

Votre application obtient les informations d’identification en appelant la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , qui retourne un handle aux informations d’identification demandées. Étant donné que les handles d’informations d’identification sont utilisés pour stocker les informations de configuration, le même handle ne peut pas être utilisé pour les opérations côté client et côté serveur. Cela signifie que les applications qui prennent en charge les connexions client et serveur doivent obtenir au moins deux handles d’informations d’identification.

dans Windows XP, une structure [**SCHANNEL \_ CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) spécifie les éléments suivants :

-   Un protocole de sécurité
-   Chiffrements autorisés
-   Puissance de chiffrement minimale et maximale
-   Un certificat [*X. 509*](../secgloss/x-gly.md) utilisé pour l’authentification, requis pour le serveur, facultatif pour le client, sauf si le serveur demande l’authentification du client.

Transmettez la structure [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (via le paramètre *pAuthData* ) à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Cette fonction retourne le handle d’informations d’identification requis pour établir un [*contexte de sécurité*](../secgloss/s-gly.md).

Pour plus d’informations sur la définition des chiffrements utilisés avec Schannel, consultez [spécification des chiffrements Schannel et des niveaux de chiffrement](specifying-schannel-ciphers-and-cipher-strengths.md).

Pour plus d’informations sur les certificats, consultez [fonctions de certificat et de magasin de certificats](../seccrypto/cryptography-functions.md).

Pour obtenir un exemple illustrant l’ouverture d’un [*magasin de certificats*](../secgloss/c-gly.md) et la localisation d’un certificat à utiliser pour l’authentification Schannel, consultez [obtention d’un certificat](getting-a-certificate-for-schannel.md).

 

 
