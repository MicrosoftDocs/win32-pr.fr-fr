---
description: Les clients et les serveurs doivent obtenir des informations d’identification avant de pouvoir établir un contexte de sécurité pour l’échange de messages.
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: Obtention des informations d’identification Digest par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123354"
---
# <a name="obtaining-default-digest-credentials"></a>Obtention des informations d’identification Digest par défaut

Les clients et les serveurs doivent obtenir des [*informations d’identification*](../secgloss/c-gly.md) avant de pouvoir établir un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages. Le comportement par défaut de la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) consiste à fournir des informations d’identification pour le principal de sécurité associé à la session d’ouverture de [*session*](../secgloss/s-gly.md)en cours.

L’exemple suivant illustre un appel côté serveur pour obtenir les informations d’identification par défaut.


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



L’appel côté client pour les informations d’identification par défaut est identique, sauf que le troisième paramètre doit spécifier SECPKG \_ cred \_ sortant pour indiquer que le client utilisera le handle d’informations d’identification retourné par la fonction.

Pour obtenir un exemple illustrant l’obtention d’informations d’identification pour un principal de sécurité autre que l’utilisateur connecté, consultez [obtention d’autres informations d’identification](obtaining-alternate-digest-credentials.md).

 

 
