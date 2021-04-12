---
description: Un code d’authentification de message (MAC) est utilisé pour détecter la falsification et la falsification de messages.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Codes d’authentification de message dans Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204162"
---
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="057c9-103">Codes d’authentification de message dans Schannel</span><span class="sxs-lookup"><span data-stu-id="057c9-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="057c9-104">Un [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac) est utilisé pour détecter la falsification et la falsification de messages.</span><span class="sxs-lookup"><span data-stu-id="057c9-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="057c9-105">L’expéditeur d’un message crée un MAC en chiffrant un [*hachage*](../secgloss/h-gly.md) unidirectionnel du corps du message à l’aide d’une [*clé de session*](../secgloss/s-gly.md) partagée par l’expéditeur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="057c9-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="057c9-106">Le MAC est ajouté au message envoyé au destinataire.</span><span class="sxs-lookup"><span data-stu-id="057c9-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="057c9-107">Le destinataire du message génère à nouveau le MAC, à l’aide de la clé de session partagée et du corps du message, et compare le MAC généré au MAC reçu de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="057c9-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="057c9-108">Si les deux sont identiques, l’expéditeur doit avoir la clé de session partagée et le message n’a pas été modifié en transit.</span><span class="sxs-lookup"><span data-stu-id="057c9-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="057c9-109">Dans les protocoles Schannel, l’algorithme utilisé pour générer le MAC est déterminé par la [suite de chiffrement](cipher-suites-in-schannel.md) utilisée par l’expéditeur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="057c9-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
