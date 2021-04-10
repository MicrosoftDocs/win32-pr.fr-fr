---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029795"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="20df8-103">IAgentBalloon::SetFontName</span><span class="sxs-lookup"><span data-stu-id="20df8-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="20df8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="20df8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="20df8-105">Définit la police affichée dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="20df8-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="20df8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="20df8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="20df8-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="20df8-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="20df8-108">BSTR qui définit la police affichée dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="20df8-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="20df8-109">La police par défaut utilisée dans la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="20df8-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="20df8-110">Vous pouvez le modifier avec **IAgentBalloon :: SetFontName**.</span><span class="sxs-lookup"><span data-stu-id="20df8-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="20df8-111">Toutefois, l’utilisateur peut remplacer le paramètre de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20df8-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="20df8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20df8-112">See Also</span></span>

[<span data-ttu-id="20df8-113">**IAgentBalloon::GetVisible**</span><span class="sxs-lookup"><span data-stu-id="20df8-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




