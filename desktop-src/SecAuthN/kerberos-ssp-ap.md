---
description: Le package d’authentification Kerberos est utilisé lors de la connexion à un réseau. les ouvertures de session locales sont gérées par MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP Kerberos/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034635"
---
# <a name="kerberos-sspap"></a>SSP Kerberos/AP

Le package d’authentification [*Kerberos*](../secgloss/k-gly.md) est utilisé lors de la connexion à un réseau. les ouvertures de session locales sont gérées par MSV1 \_ 0.

Lorsqu’un utilisateur se connecte à l’aide d’un compte réseau, par défaut, Kerberos tente de se connecter au [*Centre de distribution de clés*](../secgloss/k-gly.md) Kerberos sur le contrôleur de domaine et d’obtenir un ticket TGT (Ticket Granting Ticket) à l’aide des données de connexion fournies par l’utilisateur.

Si aucun KDC Kerberos n’est disponible, Windows utilise MSV1 \_ 0 et l’authentification directe comme décrit dans [ \_ package d’authentification MSV1 0](msv1-0-authentication-package.md).

Le package d’authentification Kerberos prend en charge la version 5, révision 6 du protocole Kerberos. Ce protocole est basé sur Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Pour plus d’informations, consultez le site Web IETF :

[https://www.ietf.org](https://www.ietf.org/)

Pour plus d’informations sur Kerberos, consultez [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Formats d’informations d’identification Kerberos

Les [*informations d’identification*](../secgloss/c-gly.md) de l’utilisateur affectées par le package d’authentification Kerberos après une tentative de connexion réussie sont un ticket et une clé de chiffrement temporaire, souvent appelée [*clé de session*](../secgloss/s-gly.md). Le ticket contient à la fois une copie chiffrée des informations d’identification du client et la clé de session.

 

 
