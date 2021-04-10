---
title: Arborescence du nom MIB
description: L’espace de noms pour les identificateurs d’objet MIB est hiérarchique. Elle est structurée de sorte que chaque objet gérable peut recevoir un nom global unique.
ms.assetid: eb3c855c-b36b-4675-8df4-e11c128b2b34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d77b0cb4c64d9645f54ec7416c45ba1a4620ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029538"
---
# <a name="mib-name-tree"></a><span data-ttu-id="ab698-104">Arborescence du nom MIB</span><span class="sxs-lookup"><span data-stu-id="ab698-104">MIB Name Tree</span></span>

<span data-ttu-id="ab698-105">L’espace de noms pour les identificateurs d’objet MIB est hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="ab698-105">The name space for MIB object identifiers is hierarchical.</span></span> <span data-ttu-id="ab698-106">Elle est structurée de sorte que chaque objet gérable peut recevoir un nom global unique.</span><span class="sxs-lookup"><span data-stu-id="ab698-106">It is structured so that each manageable object can be assigned a globally unique name.</span></span>

<span data-ttu-id="ab698-107">L’autorité pour les parties de l’espace de noms est affectée à des organisations individuelles.</span><span class="sxs-lookup"><span data-stu-id="ab698-107">Authority for parts of the name space is assigned to individual organizations.</span></span> <span data-ttu-id="ab698-108">Cela permet aux organisations d’attribuer des noms sans consulter une autorité Internet pour chaque affectation.</span><span class="sxs-lookup"><span data-stu-id="ab698-108">This allows organizations to assign names without consulting an Internet authority for each assignment.</span></span> <span data-ttu-id="ab698-109">Par exemple, l’espace de noms attribué à Microsoft est 1.3.6.1.4.1.311, qui est défini dans MSFT. MIB.</span><span class="sxs-lookup"><span data-stu-id="ab698-109">For example, the name space assigned to Microsoft is 1.3.6.1.4.1.311, which is defined in MSFT.MIB.</span></span> <span data-ttu-id="ab698-110">Microsoft a l’autorité pour attribuer des noms à des objets situés en dessous de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="ab698-110">Microsoft has the authority to assign names to objects anywhere below that name space.</span></span>

<span data-ttu-id="ab698-111">L’identificateur d’objet dans la hiérarchie est écrit sous la forme d’une séquence de sous-identificateurs commençant à la racine et se terminant à l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab698-111">The object identifier in the hierarchy is written as a sequence of subidentifiers beginning at the root and ending at the object.</span></span> <span data-ttu-id="ab698-112">Les sous-identificateurs sont séparés par un point.</span><span class="sxs-lookup"><span data-stu-id="ab698-112">Subidentifiers are separated with a period.</span></span>

 

 




