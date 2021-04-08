---
title: Informations d’erreur étendues pour l’utilisateur
description: Si des informations d’erreur étendues sont disponibles, les composants qui participent à la création des informations d’erreur étendues doivent faciliter la recherche du problème.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840186"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="b6588-103">Informations d’erreur étendues pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b6588-103">Extended Error Information for the User</span></span>

<span data-ttu-id="b6588-104">Si des informations d’erreur étendues sont disponibles, les composants qui participent à la création des informations d’erreur étendues doivent faciliter la recherche du problème.</span><span class="sxs-lookup"><span data-stu-id="b6588-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="b6588-105">La première étape consiste à examiner le dernier enregistrement d’erreur étendue et à déterminer sur quel ordinateur et de quelle façon le problème provient.</span><span class="sxs-lookup"><span data-stu-id="b6588-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="b6588-106">Il s’agit souvent de la cause de l' \_ erreur RPC S \_ \* .</span><span class="sxs-lookup"><span data-stu-id="b6588-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="b6588-107">Recherchez l’emplacement de détection et déterminez ce que signifient les paramètres de cet emplacement de détection.</span><span class="sxs-lookup"><span data-stu-id="b6588-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="b6588-108">En règle générale, elles indiquent l’échec d’un appel de fonction ou d’une vérification particulière.</span><span class="sxs-lookup"><span data-stu-id="b6588-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="b6588-109">À partir de là, déterminez la raison de l’échec de la fonction ou de la vérification et prenez des mesures correctives.</span><span class="sxs-lookup"><span data-stu-id="b6588-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="b6588-110">Les enregistrements qui précèdent le dernier enregistrement indiquent le chemin d’accès de l’erreur et constituent généralement un contrôle de validité plutôt qu’une aide dans le processus de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b6588-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




