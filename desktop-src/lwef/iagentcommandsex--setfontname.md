---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671638"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="ef82c-103">IAgentCommandsEx::SetFontName</span><span class="sxs-lookup"><span data-stu-id="ef82c-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="ef82c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef82c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="ef82c-105">Définit la police affichée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="ef82c-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="ef82c-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ef82c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ef82c-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="ef82c-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="ef82c-108">BSTR qui définit la police affichée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="ef82c-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="ef82c-109">Cette propriété détermine la police utilisée pour afficher le texte dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="ef82c-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="ef82c-110">La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère, ou si ce n’est pas le cas, le paramètre ID de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef82c-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="ef82c-111">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="ef82c-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef82c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef82c-112">See Also</span></span>

<span data-ttu-id="ef82c-113">[**IAgentCommandsEx :: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx :: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx :: SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="ef82c-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




