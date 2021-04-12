---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311602"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="09cbe-103">IAgentCharacter :: GetName</span><span class="sxs-lookup"><span data-stu-id="09cbe-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="09cbe-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09cbe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="09cbe-105">Récupère le nom du caractère.</span><span class="sxs-lookup"><span data-stu-id="09cbe-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="09cbe-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="09cbe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="09cbe-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="09cbe-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="09cbe-108">Adresse d’un BSTR qui reçoit la valeur du nom pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="09cbe-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="09cbe-109">Le nom par défaut d’un caractère est défini lorsqu’il est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="09cbe-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="09cbe-110">Le nom d’un caractère peut varier en fonction de l’ID de langue du caractère.</span><span class="sxs-lookup"><span data-stu-id="09cbe-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="09cbe-111">Les caractères peuvent être compilés avec des noms différents dans différentes langues.</span><span class="sxs-lookup"><span data-stu-id="09cbe-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="09cbe-112">Vous pouvez également définir le nom du caractère à l’aide de **IAgentCharacter : SetName**; Toutefois, cela modifie le nom de tous les clients actuels du caractère.</span><span class="sxs-lookup"><span data-stu-id="09cbe-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="09cbe-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09cbe-113">See Also</span></span>

[<span data-ttu-id="09cbe-114">**IAgentCharacter :: SetName**</span><span class="sxs-lookup"><span data-stu-id="09cbe-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 




