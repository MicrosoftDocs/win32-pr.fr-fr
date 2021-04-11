---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311215"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="93347-103">IAgentBalloon::SetFontSize</span><span class="sxs-lookup"><span data-stu-id="93347-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="93347-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93347-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="93347-105">Définit la taille de la police affichée dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="93347-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="93347-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="93347-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="93347-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="93347-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="93347-108">Taille de la police.</span><span class="sxs-lookup"><span data-stu-id="93347-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="93347-109">La taille de police par défaut utilisée dans la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="93347-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="93347-110">Vous pouvez le modifier avec **IAgentBalloon :: SetFontSize**.</span><span class="sxs-lookup"><span data-stu-id="93347-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="93347-111">Toutefois, l’utilisateur peut remplacer le paramètre de taille de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93347-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="93347-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93347-112">See Also</span></span>

[<span data-ttu-id="93347-113">**IAgentBalloon::GetFontSize**</span><span class="sxs-lookup"><span data-stu-id="93347-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




