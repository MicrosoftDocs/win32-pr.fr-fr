---
description: Explique comment utiliser la prise en charge des messages SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Utilisation de la prise en charge des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530147"
---
# <a name="using-message-support"></a><span data-ttu-id="5bb30-103">Utilisation de la prise en charge des messages</span><span class="sxs-lookup"><span data-stu-id="5bb30-103">Using Message Support</span></span>

<span data-ttu-id="5bb30-104">Une fois qu’une négociation est terminée et qu’une connexion sécurisée a été établie, une application peut utiliser les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)et [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) pour échanger des données d’application signées ou chiffrées avec l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="5bb30-104">After a handshake has been completed and a secure connection has been established, an application can use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature), and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions to exchange signed or encrypted application data with the remote computer.</span></span>

<span data-ttu-id="5bb30-105">Les exemples qui utilisent ces fonctions après l’établissement d’un [*contexte de sécurité*](../secgloss/s-gly.md) sont présentés dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="5bb30-105">Examples that use these functions after a [*security context*](../secgloss/s-gly.md) has been established are demonstrated in the following sections:</span></span>

-   [<span data-ttu-id="5bb30-106">Signature d’un message</span><span class="sxs-lookup"><span data-stu-id="5bb30-106">Signing a Message</span></span>](signing-a-message.md)
-   [<span data-ttu-id="5bb30-107">Vérification d’un message</span><span class="sxs-lookup"><span data-stu-id="5bb30-107">Verifying a Message</span></span>](verifying-a-message.md)
-   [<span data-ttu-id="5bb30-108">Chiffrement d’un message</span><span class="sxs-lookup"><span data-stu-id="5bb30-108">Encrypting a Message</span></span>](encrypting-a-message.md)
-   [<span data-ttu-id="5bb30-109">Déchiffrement d’un message</span><span class="sxs-lookup"><span data-stu-id="5bb30-109">Decrypting a Message</span></span>](decrypting-a-message.md)

 

 
