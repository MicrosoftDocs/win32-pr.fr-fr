---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380047"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="7aba2-103">IAgentCommandsEx::GetFontSize</span><span class="sxs-lookup"><span data-stu-id="7aba2-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="7aba2-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7aba2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="7aba2-105">Récupère la valeur de la taille de la police affichée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="7aba2-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="7aba2-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7aba2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7aba2-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="7aba2-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="7aba2-108">Adresse d’une valeur qui reçoit la taille de la police.</span><span class="sxs-lookup"><span data-stu-id="7aba2-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="7aba2-109">La taille en points de la police retournée correspond à la taille définie pour afficher le texte dans le menu contextuel du caractère lorsque votre client est en entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="7aba2-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="7aba2-110">La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère ou, si elle n’est pas définie, sur le paramètre de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7aba2-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="7aba2-111">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="7aba2-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="7aba2-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7aba2-112">See Also</span></span>

<span data-ttu-id="7aba2-113">[**IAgentCommandsEx :: SetFontSize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx :: SetFontName**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="7aba2-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




