---
title: Que pouvez-vous savoir, et quand le savoir
description: Les applications sensibles aux États induits par la latence doivent reconnaître les États des problèmes et prendre les mesures appropriées.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541811"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="63a6d-103">Que pouvez-vous savoir, et quand pouvez-vous le savoir ?</span><span class="sxs-lookup"><span data-stu-id="63a6d-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="63a6d-104">Les applications sensibles aux États induits par la latence doivent reconnaître les États des problèmes et prendre les mesures appropriées.</span><span class="sxs-lookup"><span data-stu-id="63a6d-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="63a6d-105">Deux États posent problème : le décalage de version et la mise à jour partielle.</span><span class="sxs-lookup"><span data-stu-id="63a6d-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="63a6d-106">Le décalage de version n’est pas détectable en examinant le service d’annuaire (n’oubliez pas le axiome de l’informatique distribuée indiqué dans [pourquoi Active Directory Domain Services utiliser ce modèle de réplication](why-active-directory-domain-services-uses-this-replication-model.md)).</span><span class="sxs-lookup"><span data-stu-id="63a6d-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="63a6d-107">Une mise à jour partielle peut être détectée en ajoutant des métadonnées aux objets qui composent le jeu associé.</span><span class="sxs-lookup"><span data-stu-id="63a6d-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="63a6d-108">Des suggestions pour ces métadonnées s’affichent dans les sections suivantes de ce document.</span><span class="sxs-lookup"><span data-stu-id="63a6d-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="63a6d-109">Certaines stratégies d’évitement peuvent être nécessaires pour réduire le risque de décalage de version et de mise à jour partielle.</span><span class="sxs-lookup"><span data-stu-id="63a6d-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="63a6d-110">Ces stratégies sont également abordées dans les sections suivantes de ce document.</span><span class="sxs-lookup"><span data-stu-id="63a6d-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




