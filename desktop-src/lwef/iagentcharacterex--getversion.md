---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029023"
---
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="d7924-103">IAgentCharacterEx :: GetVersion</span><span class="sxs-lookup"><span data-stu-id="d7924-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="d7924-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7924-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="d7924-105">Récupère le numéro de version de l’ensemble d’animations standard de caractères.</span><span class="sxs-lookup"><span data-stu-id="d7924-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="d7924-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d7924-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d7924-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="d7924-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="d7924-108">Adresse d’une variable qui reçoit la version principale.</span><span class="sxs-lookup"><span data-stu-id="d7924-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="d7924-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="d7924-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="d7924-110">Adresse d’une variable qui reçoit la version mineure.</span><span class="sxs-lookup"><span data-stu-id="d7924-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="d7924-111">Le numéro de version du jeu d’animations standard est défini automatiquement quand vous le générez avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d7924-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 




