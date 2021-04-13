---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380048"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="71bc6-103">IAgentCommandsEx::GetFontName</span><span class="sxs-lookup"><span data-stu-id="71bc6-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="71bc6-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71bc6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="71bc6-105">Récupère la valeur de la police affichée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="71bc6-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="71bc6-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="71bc6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="71bc6-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="71bc6-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="71bc6-108">Adresse d’un BSTR qui reçoit le nom de la police affiché dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="71bc6-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="71bc6-109">Le nom de police retourné correspond à la police utilisée pour afficher le texte dans le menu contextuel du caractère lorsque votre application cliente est en entrée active.</span><span class="sxs-lookup"><span data-stu-id="71bc6-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="71bc6-110">La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère ou, si elle n’est pas définie, sur le paramètre ID de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71bc6-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="71bc6-111">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="71bc6-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="71bc6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71bc6-112">See Also</span></span>

<span data-ttu-id="71bc6-113">[**IAgentCommandsEx :: SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx :: SetFontSize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="71bc6-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




