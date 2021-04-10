---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940167"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="0c6be-103">IAgentCharacterEx :: GetGUID</span><span class="sxs-lookup"><span data-stu-id="0c6be-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="0c6be-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c6be-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="0c6be-105">Récupère l’ID unique du caractère.</span><span class="sxs-lookup"><span data-stu-id="0c6be-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="0c6be-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0c6be-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0c6be-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span><span class="sxs-lookup"><span data-stu-id="0c6be-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="0c6be-108">Adresse d’un BSTR qui reçoit l’ID du caractère.</span><span class="sxs-lookup"><span data-stu-id="0c6be-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="0c6be-109">La propriété retourne une représentation sous forme de chaîne du GUID (mis en forme à l’aide d’accolades et de tirets) que le serveur utilise pour identifier le caractère de manière unique.</span><span class="sxs-lookup"><span data-stu-id="0c6be-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="0c6be-110">Un identificateur de caractère est défini lorsqu’il est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0c6be-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0c6be-111">la propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0c6be-111">The property is read-only.</span></span>

 

 




