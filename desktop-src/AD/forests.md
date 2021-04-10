---
title: Forêts
description: Une forêt est un ensemble d’une ou plusieurs arborescences de domaines qui ne forment pas un espace de noms contigu.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- forêts Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940820"
---
# <a name="forests"></a><span data-ttu-id="217cb-104">Forêts</span><span class="sxs-lookup"><span data-stu-id="217cb-104">Forests</span></span>

<span data-ttu-id="217cb-105">Une [*forêt*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) est un ensemble d’une ou plusieurs arborescences de domaines qui ne forment pas un espace de noms contigu.</span><span class="sxs-lookup"><span data-stu-id="217cb-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="217cb-106">Toutes les arborescences d’une forêt partagent un schéma, une configuration et un catalogue global communs.</span><span class="sxs-lookup"><span data-stu-id="217cb-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="217cb-107">Toutes les arborescences d’une forêt donnée font confiance à Exchange en fonction des relations d’approbation Kerberos transitives hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="217cb-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="217cb-108">Contrairement aux arborescences, une forêt ne nécessite pas de nom distinct.</span><span class="sxs-lookup"><span data-stu-id="217cb-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="217cb-109">Une forêt existe sous la forme d’un ensemble d’objets de référence croisée et de relations d’approbation Kerberos reconnues par les arborescences membres.</span><span class="sxs-lookup"><span data-stu-id="217cb-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="217cb-110">Les arborescences d’une forêt forment une hiérarchie à des fins d’approbation Kerberos ; le nom de l’arborescence à la racine de l’arborescence d’approbation fait référence à une forêt donnée.</span><span class="sxs-lookup"><span data-stu-id="217cb-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="217cb-111">L’illustration suivante montre une forêt d’espaces de noms non contigus.</span><span class="sxs-lookup"><span data-stu-id="217cb-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![forêt d’espaces de noms non contigus](images/forests.png)

 

 