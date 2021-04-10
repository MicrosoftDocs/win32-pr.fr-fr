---
title: Arborescences de domaines
description: Une arborescence de domaine est constituée de plusieurs domaines qui partagent un schéma et une configuration communs, formant un espace de noms contigu.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory de l’arborescence de domaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190774"
---
# <a name="domain-trees"></a><span data-ttu-id="3c206-104">Arborescences de domaines</span><span class="sxs-lookup"><span data-stu-id="3c206-104">Domain Trees</span></span>

<span data-ttu-id="3c206-105">Une *arborescence de domaine* est constituée de plusieurs domaines qui partagent un schéma et une configuration communs, formant un espace de noms contigu.</span><span class="sxs-lookup"><span data-stu-id="3c206-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="3c206-106">Les domaines d’une arborescence sont également liés par des relations d’approbation.</span><span class="sxs-lookup"><span data-stu-id="3c206-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="3c206-107">Active Directory est un ensemble d’une ou plusieurs arborescences.</span><span class="sxs-lookup"><span data-stu-id="3c206-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="3c206-108">Les arborescences peuvent être consultées de deux façons.</span><span class="sxs-lookup"><span data-stu-id="3c206-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="3c206-109">Une vue est celle des relations d’approbation entre les domaines.</span><span class="sxs-lookup"><span data-stu-id="3c206-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="3c206-110">L’autre vue est l’espace de noms de l’arborescence de domaine.</span><span class="sxs-lookup"><span data-stu-id="3c206-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="3c206-111">Affichage des relations d’approbation</span><span class="sxs-lookup"><span data-stu-id="3c206-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="3c206-112">Vous pouvez dessiner un diagramme d’une arborescence de domaine en fonction des domaines individuels et de la relation d’approbation existante.</span><span class="sxs-lookup"><span data-stu-id="3c206-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="3c206-113">Windows 2000 établit des relations d’approbation entre les domaines selon le protocole de sécurité Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3c206-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="3c206-114">L’approbation Kerberos est transitive et hiérarchique : si le domaine A approuve le domaine B et que le domaine B approuve le domaine C, le domaine A approuve le domaine C.</span><span class="sxs-lookup"><span data-stu-id="3c206-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![relation d’approbation de l’arborescence de domaine](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="3c206-116">Affichage de l’espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c206-116">Viewing the Namespace</span></span>

<span data-ttu-id="3c206-117">Vous pouvez également dessiner un diagramme d’une arborescence de domaine en fonction de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="3c206-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="3c206-118">Vous pouvez déterminer le nom unique d’un objet en suivant le chemin d’accès vers le haut de la hiérarchie de l’espace de noms de l’arborescence de domaine.</span><span class="sxs-lookup"><span data-stu-id="3c206-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="3c206-119">Cette vue est utile pour regrouper des objets dans une hiérarchie logique.</span><span class="sxs-lookup"><span data-stu-id="3c206-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="3c206-120">Le principal avantage d’un espace de noms contigu est qu’une recherche profonde depuis la racine de l’espace de noms recherche dans l’ensemble de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3c206-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![arborescence du domaine de l’espace de noms](images/namespace.png)

 

 




