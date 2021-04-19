---
description: Explique comment protéger les messages à l’aide de Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protection des messages à l’aide de Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528182"
---
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="c7ff1-103">Protection des messages à l’aide de Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="c7ff1-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="c7ff1-104">HTTP et SASL</span><span class="sxs-lookup"><span data-stu-id="c7ff1-104">HTTP and SASL</span></span>

<span data-ttu-id="c7ff1-105">Pour détecter certains types de violations de sécurité, le client et le serveur utilisent les fonctions d' [*intégrité*](../secgloss/i-gly.md) des messages SSPI ( [Security Support Provider Interface](sspi.md) ) [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) pour protéger les messages.</span><span class="sxs-lookup"><span data-stu-id="c7ff1-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="c7ff1-106">Un client appelle la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour signer un message à l’aide de son [*contexte de sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c7ff1-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c7ff1-107">Le serveur utilise la fonction [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) pour vérifier l’origine du message.</span><span class="sxs-lookup"><span data-stu-id="c7ff1-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="c7ff1-108">En plus de vérifier la [*signature*](../secgloss/d-gly.md) qui accompagne le message, la fonction **VerifySignature** vérifie également que le nombre de [*nonce*](../secgloss/n-gly.md) (spécifié par la directive NC) est supérieur au dernier nombre envoyé pour la valeur à usage unique.</span><span class="sxs-lookup"><span data-stu-id="c7ff1-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="c7ff1-109">Si ce n’est pas le cas, la fonction **VerifySignature** retourne un \_ \_ code d’erreur en dehors de la \_ séquence.</span><span class="sxs-lookup"><span data-stu-id="c7ff1-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="c7ff1-110">SASL uniquement</span><span class="sxs-lookup"><span data-stu-id="c7ff1-110">SASL Only</span></span>

<span data-ttu-id="c7ff1-111">Les fonctions [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) et [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) fournissent la confidentialité des messages postérieurs à l’authentification échangés entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="c7ff1-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="c7ff1-112">Pour pouvoir utiliser les fonctions de confidentialité des messages, le serveur et le client doivent avoir établi un [*contexte de sécurité*](../secgloss/s-gly.md) avec les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="c7ff1-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="c7ff1-113">La qualité de protection, spécifiée par la directive QoP, doit être « auth-CONF ».</span><span class="sxs-lookup"><span data-stu-id="c7ff1-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="c7ff1-114">Un mécanisme de chiffrement doit avoir été spécifié au moyen de la directive de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c7ff1-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 
