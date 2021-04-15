---
title: Localité temporelle
description: La localité temporelle est une stratégie d’évitement qui réduit la fenêtre pour les mises à jour partielles.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462003"
---
# <a name="temporal-locality"></a><span data-ttu-id="5419d-103">Localité temporelle</span><span class="sxs-lookup"><span data-stu-id="5419d-103">Temporal Locality</span></span>

<span data-ttu-id="5419d-104">La *localité temporelle* est une stratégie d’évitement qui réduit la fenêtre pour les mises à jour partielles.</span><span class="sxs-lookup"><span data-stu-id="5419d-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="5419d-105">La réplication des modifications à partir d’un réplica source donné se poursuit par ordre USN croissant.</span><span class="sxs-lookup"><span data-stu-id="5419d-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="5419d-106">Les écritures qui se produisent de façon rapprochée dans le temps comportent des USN qui sont « proches » les uns des autres et qui sont propagés de façon rapprochée dans le temps.</span><span class="sxs-lookup"><span data-stu-id="5419d-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="5419d-107">Les applications qui créent ou mettent à jour plusieurs objets connexes doivent écrire les objets le plus près possible dans le temps.</span><span class="sxs-lookup"><span data-stu-id="5419d-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="5419d-108">Par exemple, l’application peut collecter toutes les entrées nécessaires de l’utilisateur et les appliquer au répertoire lorsque l’utilisateur clique sur le bouton « appliquer ».</span><span class="sxs-lookup"><span data-stu-id="5419d-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="5419d-109">La localité temporelle réduit également les risques de résolution des collisions introduisant des incohérences intra-objets.</span><span class="sxs-lookup"><span data-stu-id="5419d-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




