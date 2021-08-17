---
description: Explique comment utiliser la prise en charge des messages SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Utilisation de la prise en charge des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c6a14c28cc9eb9e1b606574659412a22f375ad935ee0d7d1bdd898781c230d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785919"
---
# <a name="using-message-support"></a>Utilisation de la prise en charge des messages

Une fois qu’une négociation est terminée et qu’une connexion sécurisée a été établie, une application peut utiliser les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)et [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) pour échanger des données d’application signées ou chiffrées avec l’ordinateur distant.

Les exemples qui utilisent ces fonctions après l’établissement d’un [*contexte de sécurité*](../secgloss/s-gly.md) sont présentés dans les sections suivantes :

-   [Signature d’un message](signing-a-message.md)
-   [Vérification d’un message](verifying-a-message.md)
-   [Chiffrement d’un message](encrypting-a-message.md)
-   [Déchiffrement d’un message](decrypting-a-message.md)

 

 
