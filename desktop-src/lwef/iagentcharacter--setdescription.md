---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380439"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="2f559-103">IAgentCharacter :: SetDescription</span><span class="sxs-lookup"><span data-stu-id="2f559-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="2f559-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f559-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="2f559-105">Définit la description du caractère.</span><span class="sxs-lookup"><span data-stu-id="2f559-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="2f559-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2f559-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2f559-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span><span class="sxs-lookup"><span data-stu-id="2f559-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="2f559-108">BSTR qui définit la description du caractère.</span><span class="sxs-lookup"><span data-stu-id="2f559-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="2f559-109">La description par défaut d’un caractère est définie lorsqu’elle est compilée avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2f559-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="2f559-110">Le paramètre description est facultatif et ne peut pas être fourni pour tous les caractères.</span><span class="sxs-lookup"><span data-stu-id="2f559-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="2f559-111">Vous pouvez modifier la description du caractère à l’aide de **IAgentCharacter :: SetDescription**; Toutefois, cette valeur n’est pas persistante (stockée de façon permanente).</span><span class="sxs-lookup"><span data-stu-id="2f559-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="2f559-112">La description du caractère revient à sa valeur par défaut chaque fois que le caractère est chargé pour la première fois par un client.</span><span class="sxs-lookup"><span data-stu-id="2f559-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2f559-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f559-113">See Also</span></span>

[<span data-ttu-id="2f559-114">**IAgentCharacter :: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="2f559-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 




