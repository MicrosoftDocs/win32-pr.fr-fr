---
description: Les terminaux enfichables permettent à une application de créer des terminaux au moment de l’exécution.
ms.assetid: 34ba4f3c-0a14-4705-9490-817c70700746
title: Terminaux enfichables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52802d98d7eb6985dbb7de9ca3facab90a5550e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536393"
---
# <a name="pluggable-terminals"></a><span data-ttu-id="83f56-103">Terminaux enfichables</span><span class="sxs-lookup"><span data-stu-id="83f56-103">Pluggable Terminals</span></span>

<span data-ttu-id="83f56-104">Les terminaux enfichables permettent à une application de créer des terminaux au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="83f56-104">Pluggable terminals allow an application to create terminals during run time.</span></span> <span data-ttu-id="83f56-105">Les terminaux sont normalement créés et contrôlés par une paire fournisseur de services de téléphonie/fournisseur de services de média (TSP/MSP), ce qui reste le moyen le plus polyvalent et le plus stable de manipuler les terminaux.</span><span class="sxs-lookup"><span data-stu-id="83f56-105">Terminals are normally created and controlled by a telephony service provider/media service provider (TSP/MSP) pair, and this remains the most versatile and stable means of manipulating terminals.</span></span> <span data-ttu-id="83f56-106">Toutefois, certaines applications doivent utiliser des terminaux simples dans les situations où une paire TSP/MSP appropriée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="83f56-106">However, some applications need to use simple terminals in situations where an appropriate TSP/MSP pair is not available.</span></span> <span data-ttu-id="83f56-107">Seuls les créateurs d’applications qui sont familiarisés avec les opérations TSP/MSP doivent utiliser des terminaux enfichables.</span><span class="sxs-lookup"><span data-stu-id="83f56-107">Only application writers who are thoroughly familiar with TSP/MSP operations should use pluggable terminals.</span></span>

<span data-ttu-id="83f56-108">Dans TAPI version 3,1, les terminaux enfichables sont ajoutés au modèle TAPI.</span><span class="sxs-lookup"><span data-stu-id="83f56-108">In TAPI version 3.1, pluggable terminals are added to the TAPI model.</span></span> <span data-ttu-id="83f56-109">Les terminaux enfichables permettent à un tiers d’ajouter un nouvel objet terminal que n’importe quel MSP peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="83f56-109">Pluggable terminals allow a third party to add a new terminal object that any MSP can use.</span></span>

<span data-ttu-id="83f56-110">Pour plus d’informations, consultez [inscription de terminal enfichable](pluggable-terminal-registration.md) et [écriture d’un terminal enfichable](writing-a-pluggable-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="83f56-110">See [Pluggable Terminal Registration](pluggable-terminal-registration.md) and [Writing a Pluggable Terminal](writing-a-pluggable-terminal.md) for more information.</span></span>

 

 



