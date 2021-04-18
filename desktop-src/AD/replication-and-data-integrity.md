---
title: Réplication et intégrité des données
description: Active Directory Domain Services fournir une mise à jour multimaître.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, réplication et intégrité des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512227"
---
# <a name="replication-and-data-integrity"></a><span data-ttu-id="adf5a-104">Réplication et intégrité des données</span><span class="sxs-lookup"><span data-stu-id="adf5a-104">Replication and Data Integrity</span></span>

<span data-ttu-id="adf5a-105">Active Directory Domain Services fournir *une mise à jour multimaître*.</span><span class="sxs-lookup"><span data-stu-id="adf5a-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="adf5a-106">La mise à jour à plusieurs maîtres signifie que tous les réplicas complets d’une partition donnée sont accessibles en écriture (les réplicas partiels sur les serveurs de catalogue global ne sont pas accessibles en écriture). Une mise à jour multimaître signifie que les mises à jour ne sont pas bloquées, même lorsque certains réplicas sont inutilisables.</span><span class="sxs-lookup"><span data-stu-id="adf5a-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="adf5a-107">Le serveur Active Directory propage les modifications à partir du réplica mis à jour vers tous les autres réplicas.</span><span class="sxs-lookup"><span data-stu-id="adf5a-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="adf5a-108">La réplication est automatique et transparente.</span><span class="sxs-lookup"><span data-stu-id="adf5a-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="adf5a-109">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="adf5a-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="adf5a-110">Le modèle de réplication dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="adf5a-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="adf5a-111">Comportement de réplication dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="adf5a-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="adf5a-112">Détection et prévention de la latence de réplication</span><span class="sxs-lookup"><span data-stu-id="adf5a-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




