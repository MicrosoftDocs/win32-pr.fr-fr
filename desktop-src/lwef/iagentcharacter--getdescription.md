---
title: GetDescription IAgentCharacter
description: GetDescription IAgentCharacter
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380447"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="6c2e0-103">IAgentCharacter :: GetDescription</span><span class="sxs-lookup"><span data-stu-id="6c2e0-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="6c2e0-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6c2e0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="6c2e0-105">Récupère la description du caractère.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="6c2e0-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6c2e0-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span><span class="sxs-lookup"><span data-stu-id="6c2e0-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="6c2e0-108">Adresse d’un BSTR qui reçoit la valeur de la description du caractère.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="6c2e0-109">La description d’un caractère est définie lorsqu’elle est compilée avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="6c2e0-110">Le paramètre description est facultatif et ne peut pas être fourni pour tous les caractères.</span><span class="sxs-lookup"><span data-stu-id="6c2e0-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 




