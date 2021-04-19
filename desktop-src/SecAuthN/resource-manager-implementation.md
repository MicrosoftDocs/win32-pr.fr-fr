---
description: Le gestionnaire des ressources s’exécute en tant que service approuvé dans un processus unique. Toutes les demandes d’accès par carte à puce sont envoyées au gestionnaire de ressources, qui les achemine vers le lecteur qui contient la carte ciblée.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implémentation de Gestionnaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517826"
---
# <a name="resource-manager-implementation"></a><span data-ttu-id="80532-104">Implémentation de Gestionnaire des ressources</span><span class="sxs-lookup"><span data-stu-id="80532-104">Resource Manager Implementation</span></span>

<span data-ttu-id="80532-105">Le [*Gestionnaire des ressources*](../secgloss/r-gly.md) s’exécute en tant que service approuvé dans un processus unique.</span><span class="sxs-lookup"><span data-stu-id="80532-105">The [*resource manager*](../secgloss/r-gly.md) runs as a trusted service in a single process.</span></span> <span data-ttu-id="80532-106">Toutes les demandes d’accès par [*carte à puce*](../secgloss/s-gly.md) sont envoyées au gestionnaire de ressources, qui les achemine vers le [*lecteur*](../secgloss/r-gly.md) qui contient la carte ciblée.</span><span class="sxs-lookup"><span data-stu-id="80532-106">All requests for [*smart card*](../secgloss/s-gly.md) access are made to the resource manager, which routes them to the [*reader*](../secgloss/r-gly.md) that contains the targeted card.</span></span>

<span data-ttu-id="80532-107">Les cartes à puce sont souvent utilisées conjointement à la sécurité et à la confidentialité personnelle.</span><span class="sxs-lookup"><span data-stu-id="80532-107">Smart cards are often used in conjunction with security and personal privacy.</span></span> <span data-ttu-id="80532-108">Dans la mesure du possible, Resource Manager utilise les mécanismes de sécurité existants dans le système d’exploitation sous-jacent lors de l’accès à un lecteur ou une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="80532-108">Wherever possible, the resource manager uses the security mechanisms existing within the underlying operating system when accessing a reader or smart card.</span></span>

 

 
