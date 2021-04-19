---
description: Toutes les opérations normales de RSA/SChannel et de Diffie-Hellman/Schannel utilisent la \_ paire de clés publique/privée à KeyExchange.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Utilisation de la paire de clés publique/privée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530650"
---
# <a name="publicprivate-key-pair-usage"></a><span data-ttu-id="00f53-103">Utilisation de la paire de clés publique/privée</span><span class="sxs-lookup"><span data-stu-id="00f53-103">Public/Private Key Pair Usage</span></span>

<span data-ttu-id="00f53-104">Toutes les opérations normales de [*RSA*](../secgloss/r-gly.md)/Schannel et [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel utilisent la \_ paire de [*clés publique/privée*](../secgloss/p-gly.md)à KeyExchange.</span><span class="sxs-lookup"><span data-stu-id="00f53-104">All normal [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel operations use the AT\_KEYEXCHANGE [*public/private key pair*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="00f53-105">Pour permettre l' [*authentification*](../secgloss/a-gly.md)du serveur, le côté serveur des opérations Schannel doit avoir accès à son certificat [*X. 509*](../secgloss/x-gly.md) contenant sa clé publique et à l’accès à la [*clé privée*](../secgloss/p-gly.md)correspondante.</span><span class="sxs-lookup"><span data-stu-id="00f53-105">To provide server [*authentication*](../secgloss/a-gly.md), the server-side of Schannel operations must have access to its [*X.509*](../secgloss/x-gly.md) certificate containing its public key and access to the matching [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="00f53-106">Le côté client de [*Schannel*](../secgloss/s-gly.md) a besoin de son certificat avec sa clé publique et d’un accès à sa clé privée si l’authentification du client est implémentée.</span><span class="sxs-lookup"><span data-stu-id="00f53-106">The client-side of [*Schannel*](../secgloss/s-gly.md) needs its certificate with its public key and access to its private key if client authentication is implemented.</span></span>

<span data-ttu-id="00f53-107">Étant donné que les moteurs de protocole Schannel n’utilisent jamais la \_ paire de clés publique/privée at signature, cette paire de clés n’a pas besoin d’être prise en charge par un nouveau fournisseur de services de chiffrement prenant uniquement en charge RSA/SChannel ou Diffie-Hellman/Schannel.</span><span class="sxs-lookup"><span data-stu-id="00f53-107">Since Schannel protocol engines never use the AT\_SIGNATURE public/private key pair, that key pair need not be supported by a new CSP supporting only RSA/Schannel or Diffie-Hellman/Schannel.</span></span>

<span data-ttu-id="00f53-108">Si un moteur de protocole utilise une suite de chiffrement d’exportation SSL 3,0 avec une \_ paire de clés at KeyExchange supérieure à 512 bits, le serveur doit utiliser une paire de clés RSA supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="00f53-108">If a protocol engine uses an SSL 3.0 export cipher suite with an AT\_KEYEXCHANGE key pair larger than 512 bits, the server must use an additional RSA key pair.</span></span> <span data-ttu-id="00f53-109">Cette paire de clés supplémentaire est toujours exactement de 512 bits et peut être éphémère.</span><span class="sxs-lookup"><span data-stu-id="00f53-109">This additional key pair is always exactly 512 bits and it can be ephemeral.</span></span> <span data-ttu-id="00f53-110">La paire est stockée en tant qu' \_ élément at KeyExchange dans un conteneur de clé détenu par le moteur de protocole.</span><span class="sxs-lookup"><span data-stu-id="00f53-110">The pair is stored as an AT\_KEYEXCHANGE element in a key container owned by the protocol engine.</span></span> <span data-ttu-id="00f53-111">Un descripteur de ce conteneur de clé est généralement acquis au démarrage du moteur de protocole.</span><span class="sxs-lookup"><span data-stu-id="00f53-111">A handle to this key container is typically acquired at protocol engine startup.</span></span>

<span data-ttu-id="00f53-112">Diffie-Hellman prend en charge uniquement [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) et utilise des clés publiques RSA ou DSS normales.</span><span class="sxs-lookup"><span data-stu-id="00f53-112">Diffie-Hellman supports only [*CALG\_DH\_EPHEM*](../secgloss/c-gly.md) and uses normal RSA or DSS public keys.</span></span>

 

 
