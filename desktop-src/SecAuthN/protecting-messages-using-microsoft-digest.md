---
description: Explique comment protéger les messages à l’aide de Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protection des messages à l’aide de Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab0add351287b6c90cfe0781151c0378da56f309214b03ed12d1325a6e55d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920738"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Protection des messages à l’aide de Microsoft Digest

## <a name="http-and-sasl"></a>HTTP et SASL

Pour détecter certains types de violations de sécurité, le client et le serveur utilisent les fonctions d' [*intégrité*](../secgloss/i-gly.md) des messages SSPI ( [Security Support Provider Interface](sspi.md) ) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) pour protéger les messages.

Un client appelle la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour signer un message à l’aide de son [*contexte de sécurité*](../secgloss/s-gly.md). Le serveur utilise la fonction [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) pour vérifier l’origine du message. En plus de vérifier la [*signature*](../secgloss/d-gly.md) qui accompagne le message, la fonction **VerifySignature** vérifie également que le nombre de [*nonce*](../secgloss/n-gly.md) (spécifié par la directive NC) est supérieur au dernier nombre envoyé pour la valeur à usage unique. Si ce n’est pas le cas, la fonction **VerifySignature** retourne un \_ \_ code d’erreur en dehors de la \_ séquence.

## <a name="sasl-only"></a>SASL uniquement

Les fonctions [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) et [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) fournissent la confidentialité des messages postérieurs à l’authentification échangés entre le client et le serveur.

Pour pouvoir utiliser les fonctions de confidentialité des messages, le serveur et le client doivent avoir établi un [*contexte de sécurité*](../secgloss/s-gly.md) avec les attributs suivants :

-   La qualité de protection, spécifiée par la directive QoP, doit être « auth-CONF ».
-   Un mécanisme de chiffrement doit avoir été spécifié au moyen de la directive de chiffrement.

 

 
