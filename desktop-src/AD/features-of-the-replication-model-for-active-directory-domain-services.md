---
title: Fonctionnalités du modèle de réplication pour Active Directory Domain Services
description: Le modèle de réplication utilisé dans Active Directory Domain Services est appelé cohérence non-maître avec convergence.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modèle de réplication
- Fonctionnalités du modèle de réplication Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512428"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a><span data-ttu-id="7b557-105">Fonctionnalités du modèle de réplication pour Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7b557-105">Features of the Replication Model for Active Directory Domain Services</span></span>

<span data-ttu-id="7b557-106">Le modèle de réplication utilisé dans Active Directory Domain Services est appelé *cohérence non-maître avec convergence*.</span><span class="sxs-lookup"><span data-stu-id="7b557-106">The replication model used in Active Directory Domain Services is called *multi-master loose consistency with convergence*.</span></span> <span data-ttu-id="7b557-107">Dans ce modèle, le répertoire peut avoir de nombreux réplicas ; un système de réplication propage les modifications apportées à un réplica donné vers tous les autres réplicas.</span><span class="sxs-lookup"><span data-stu-id="7b557-107">In this model, the directory can have many replicas; a replication system propagates changes made at any given replica to all other replicas.</span></span> <span data-ttu-id="7b557-108">Il n’est pas garanti que les réplicas soient cohérents entre eux à un moment donné (« faible cohérence »), car les modifications peuvent être appliquées à n’importe quel réplica à tout moment (« multi-maître »).</span><span class="sxs-lookup"><span data-stu-id="7b557-108">The replicas are not guaranteed to be consistent with each other at any particular time ("loose consistency"), because changes can be applied to any replica at any time ("multi-master").</span></span> <span data-ttu-id="7b557-109">Si le système est autorisé à atteindre un état stable et qu’aucune nouvelle mise à jour n’est en cours et que toutes les mises à jour précédentes ont été complètement répliquées, tous les réplicas sont assurés de converger sur le même ensemble de valeurs (« convergence »).</span><span class="sxs-lookup"><span data-stu-id="7b557-109">If the system is allowed to reach a steady state, in which no new updates are occurring and all previous updates have been completely replicated, all replicas are guaranteed to converge on the same set of values ("convergence").</span></span>

 

 




