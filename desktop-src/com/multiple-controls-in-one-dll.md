---
title: Plusieurs contrôles dans une DLL
description: Plusieurs contrôles dans une DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028642"
---
# <a name="multiple-controls-in-one-dll"></a><span data-ttu-id="4d33c-103">Plusieurs contrôles dans une DLL</span><span class="sxs-lookup"><span data-stu-id="4d33c-103">Multiple Controls in One DLL</span></span>

<span data-ttu-id="4d33c-104">Une seule DLL. ocx peut conteneur un nombre quelconque de contrôles ActiveX, ce qui simplifie la distribution et l’utilisation d’un ensemble de contrôles connexes.</span><span class="sxs-lookup"><span data-stu-id="4d33c-104">A single .ocx DLL can container any number of ActiveX controls, thus simplifying the distribution and use of a set of related controls.</span></span>

<span data-ttu-id="4d33c-105">Si vous livrez plusieurs contrôles dans une même DLL, veillez à inclure le nom du fournisseur dans chaque nom de contrôle du package.</span><span class="sxs-lookup"><span data-stu-id="4d33c-105">If you ship multiple controls in a single DLL, be sure to include the vendor name in each control name in the package.</span></span> <span data-ttu-id="4d33c-106">Inclure les noms des fournisseurs dans chaque nom de contrôle permet aux utilisateurs d’identifier facilement les contrôles dans un package.</span><span class="sxs-lookup"><span data-stu-id="4d33c-106">Including the vendors' names in each control name will enable users to easily identify controls within a package.</span></span> <span data-ttu-id="4d33c-107">Par exemple, si vous livrez une DLL qui implémente trois contrôles, Con1, Con2 et CON3, les noms des contrôles doivent être les suivants :</span><span class="sxs-lookup"><span data-stu-id="4d33c-107">For example, if you ship a DLL that implements three controls, Con1, Con2, and Con3, then the control names should be:</span></span>

-   <span data-ttu-id="4d33c-108">*Nom de votre société* Contrôle Con1</span><span class="sxs-lookup"><span data-stu-id="4d33c-108">*Your company name* Con1 Control</span></span>

-   <span data-ttu-id="4d33c-109">*Nom de votre société* Contrôle Con2</span><span class="sxs-lookup"><span data-stu-id="4d33c-109">*Your company name* Con2 Control</span></span>

-   <span data-ttu-id="4d33c-110">*Nom de votre société* Contrôle CON3</span><span class="sxs-lookup"><span data-stu-id="4d33c-110">*Your company name* Con3 Control</span></span>

 

 




