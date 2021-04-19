---
description: Les clés de session sont des clés générées pour être utilisées dans une session de communication unique.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Clés de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535573"
---
# <a name="session-keys"></a><span data-ttu-id="b99c6-103">Clés de session</span><span class="sxs-lookup"><span data-stu-id="b99c6-103">Session Keys</span></span>

<span data-ttu-id="b99c6-104">Les [*clés de session*](../secgloss/s-gly.md) sont des clés générées pour être utilisées dans une session de communication unique.</span><span class="sxs-lookup"><span data-stu-id="b99c6-104">[*Session keys*](../secgloss/s-gly.md) are keys that are generated to be used in a single communication session.</span></span> <span data-ttu-id="b99c6-105">Les clés de session sont fréquemment modifiées et sont ignorées lorsqu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b99c6-105">Session keys are frequently changed and are discarded when they are no longer needed.</span></span> <span data-ttu-id="b99c6-106">Par exemple, TLS utilise une clé de session distincte pour chaque connexion et S/MIME utilise une clé de session distincte pour chaque message électronique.</span><span class="sxs-lookup"><span data-stu-id="b99c6-106">For example, TLS uses a separate session key for each connection and S/MIME uses a separate session key for each email message.</span></span> <span data-ttu-id="b99c6-107">En général, une [*clé symétrique*](../secgloss/s-gly.md) est utilisée comme clé de session.</span><span class="sxs-lookup"><span data-stu-id="b99c6-107">Typically a [*symmetric key*](../secgloss/s-gly.md) is used as the session key.</span></span>

<span data-ttu-id="b99c6-108">Les clés de session sont volatiles.</span><span class="sxs-lookup"><span data-stu-id="b99c6-108">Session keys are volatile.</span></span> <span data-ttu-id="b99c6-109">Les applications peuvent enregistrer ces clés pour une utilisation ultérieure ou pour les transmettre à d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b99c6-109">Applications can save these keys for later use or for transmission to other users.</span></span> <span data-ttu-id="b99c6-110">Pour plus d’informations, consultez [stockage de clés de chiffrement et Exchange](cryptographic-key-storage-and-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="b99c6-110">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md).</span></span>

 

 
