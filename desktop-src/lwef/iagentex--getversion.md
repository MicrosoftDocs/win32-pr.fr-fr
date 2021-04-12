---
title: IAgentEx GetVersion
description: IAgentEx GetVersion
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310469"
---
# <a name="iagentexgetversion"></a><span data-ttu-id="2db95-103">IAgentEx :: GetVersion</span><span class="sxs-lookup"><span data-stu-id="2db95-103">IAgentEx::GetVersion</span></span>

<span data-ttu-id="2db95-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2db95-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="2db95-105">Récupère le numéro de version du serveur Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2db95-105">Retrieves the version number of Microsoft Agent server.</span></span>

-   <span data-ttu-id="2db95-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2db95-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2db95-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="2db95-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="2db95-108">Adresse d’une variable qui reçoit la version principale.</span><span class="sxs-lookup"><span data-stu-id="2db95-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="2db95-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="2db95-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="2db95-110">Adresse d’une variable qui reçoit la version mineure.</span><span class="sxs-lookup"><span data-stu-id="2db95-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

 

 




