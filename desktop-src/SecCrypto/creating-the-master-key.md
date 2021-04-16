---
description: Une clé principale est un matériau de données clé à partir duquel d’autres clés sont dérivées.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Création de la clé principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525738"
---
# <a name="creating-the-master-key"></a><span data-ttu-id="58566-103">Création de la clé principale</span><span class="sxs-lookup"><span data-stu-id="58566-103">Creating the Master Key</span></span>

<span data-ttu-id="58566-104">Une [*clé principale*](../secgloss/m-gly.md) est un matériau de données clé à partir duquel d’autres clés sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="58566-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="58566-105">En fonction du protocole et de la suite de chiffrement utilisés, la longueur de la clé principale peut être comprise entre 5 et 48 octets.</span><span class="sxs-lookup"><span data-stu-id="58566-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="58566-106">Pour le [](../secgloss/r-gly.md) / fournisseur CSP RSA [*Schannel*](../secgloss/s-gly.md) , la clé principale est créée par le côté client et transférée vers le serveur dans une enveloppe RSA.</span><span class="sxs-lookup"><span data-stu-id="58566-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="58566-107">Pour un CSP/Schannel [*Diffie-Hellman*](../secgloss/d-gly.md), la clé principale est créée en effectuant une Diffie-Hellman échange de clés.</span><span class="sxs-lookup"><span data-stu-id="58566-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="58566-108">Le code pour la création et l’échange de clés principales est illustré dans :</span><span class="sxs-lookup"><span data-stu-id="58566-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="58566-109">Code client Diffie-Hellman pour la création de la clé principale</span><span class="sxs-lookup"><span data-stu-id="58566-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="58566-110">Code serveur Diffie-Hellman pour la création de la clé principale</span><span class="sxs-lookup"><span data-stu-id="58566-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="58566-111">Code client RSA pour la création de la clé principale</span><span class="sxs-lookup"><span data-stu-id="58566-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="58566-112">Code du serveur RSA pour la création de la clé principale</span><span class="sxs-lookup"><span data-stu-id="58566-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="58566-113">Spécification des algorithmes</span><span class="sxs-lookup"><span data-stu-id="58566-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 
