---
description: Après l’établissement d’un contexte de sécurité, l’application peut utiliser les fonctions de prise en charge des messages pour transmettre des messages résistants aux falsifications.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantir l’intégrité des communications pendant l’échange de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112690"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a><span data-ttu-id="c8107-103">Garantir l’intégrité des communications pendant l’échange de messages</span><span class="sxs-lookup"><span data-stu-id="c8107-103">Ensuring Communication Integrity During Message Exchange</span></span>

<span data-ttu-id="c8107-104">Après l’établissement d’un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) , l’application peut utiliser les fonctions de [prise en charge des messages](authentication-functions.md) pour transmettre des messages résistants aux falsifications.</span><span class="sxs-lookup"><span data-stu-id="c8107-104">After a [*security context*](/windows/desktop/SecGloss/s-gly) is established, the application can use the [message support](authentication-functions.md) functions to transmit tamper-resistant messages.</span></span>

<span data-ttu-id="c8107-105">Le client ou le serveur transmet le contexte de sécurité et un message à la fonction [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) pour générer une signature sécurisée qui empêche la modification du message en cours de transit.</span><span class="sxs-lookup"><span data-stu-id="c8107-105">The client or server passes the security context and a message to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a secure signature that prevents the message from being modified while in transit.</span></span> <span data-ttu-id="c8107-106">Le récepteur du message appelle la fonction [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="c8107-106">The receiver of the message calls the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function.</span></span> <span data-ttu-id="c8107-107">**VerifySignature** utilise les informations de la signature pour vérifier que le message reçu n’a pas été modifié lors de la transmission.</span><span class="sxs-lookup"><span data-stu-id="c8107-107">**VerifySignature** uses the information in the signature to verify that the message received was not modified during transmission.</span></span> <span data-ttu-id="c8107-108">Le client et le serveur peuvent également échanger des messages chiffrés à l’aide de [**EncryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) et [**DecryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="c8107-108">The client and server can also exchange encrypted messages using [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span>

<span data-ttu-id="c8107-109">Le serveur dans une connexion authentifiée peut également établir des connexions avec d’autres ordinateurs distants dans le nom du client après avoir appelé [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="c8107-109">The server in an authenticated connection can also make connections with other remote computers in the name of the client after calling [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span></span>

 

 
