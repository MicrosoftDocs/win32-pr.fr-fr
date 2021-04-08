---
description: Parfois, un message signé requiert une contre-signature.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Contre-signatures de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752125"
---
# <a name="message-countersignatures"></a><span data-ttu-id="15cee-103">Contre-signatures de messages</span><span class="sxs-lookup"><span data-stu-id="15cee-103">Message Countersignatures</span></span>

<span data-ttu-id="15cee-104">Parfois, un message signé requiert une contre- [*signature*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="15cee-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="15cee-105">Par exemple, l’utilisateur A peut envoyer un message signé aux données à l’utilisateur B, en attendant que B confirme un accord avec les termes contenus dans le document.</span><span class="sxs-lookup"><span data-stu-id="15cee-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="15cee-106">L’utilisateur B décode le message, lit les termes et, si dans l’accord, en contresigné le message.</span><span class="sxs-lookup"><span data-stu-id="15cee-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="15cee-107">Le message contresigné est ensuite renvoyé à l’utilisateur A. l’utilisateur A sait maintenant et peut prouver que l’utilisateur B a accepté les conditions.</span><span class="sxs-lookup"><span data-stu-id="15cee-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="15cee-108">Le tableau suivant répertorie les sections qui contiennent des descriptions de procédure ou des exemples de programme C de signature de message.</span><span class="sxs-lookup"><span data-stu-id="15cee-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="15cee-109">Section</span><span class="sxs-lookup"><span data-stu-id="15cee-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="15cee-110">Contents</span><span class="sxs-lookup"><span data-stu-id="15cee-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="15cee-111">Fonctions de message</span><span class="sxs-lookup"><span data-stu-id="15cee-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="15cee-112">Répertorie les fonctions de signature de compteur.</span><span class="sxs-lookup"><span data-stu-id="15cee-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="15cee-113">Contre-signature d’un message</span><span class="sxs-lookup"><span data-stu-id="15cee-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="15cee-114">Détaille le processus de signature de compteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="15cee-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="15cee-115">Vérification d’une contre-signature</span><span class="sxs-lookup"><span data-stu-id="15cee-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="15cee-116">Détaille la procédure de vérification d’une signature de compteur.</span><span class="sxs-lookup"><span data-stu-id="15cee-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="15cee-117">Vérification d’un message signé</span><span class="sxs-lookup"><span data-stu-id="15cee-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="15cee-118">Décrit en détail un processus de vérification de la signature d’un message signé.</span><span class="sxs-lookup"><span data-stu-id="15cee-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="15cee-119">Exemple de programme C : encodage et décodage d’un message contresigné</span><span class="sxs-lookup"><span data-stu-id="15cee-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="15cee-120">Exemple de programme C qui encode et décode un message contresigné.</span><span class="sxs-lookup"><span data-stu-id="15cee-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
