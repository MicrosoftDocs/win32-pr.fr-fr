---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940022"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="087ec-103">IAgentCharacterEx::SetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="087ec-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="087ec-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="087ec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="087ec-105">Définit si le serveur affiche automatiquement le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="087ec-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="087ec-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="087ec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="087ec-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="087ec-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="087ec-108">Indicateur d’affichage automatique du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="087ec-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="087ec-109">Si ce paramètre est défini sur **true**, Microsoft Agent affiche automatiquement le menu contextuel du caractère lorsque l’utilisateur clique avec le bouton droit sur l’icône de barre des tâches caractère ou caractère.</span><span class="sxs-lookup"><span data-stu-id="087ec-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="087ec-110">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="087ec-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="087ec-111">En affectant à cette propriété la **valeur false**, vous pouvez créer votre propre comportement de gestion de menus.</span><span class="sxs-lookup"><span data-stu-id="087ec-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="087ec-112">Pour afficher le menu après avoir défini cette propriété sur **false**, utilisez la méthode [**IAgentCharacterEx :: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="087ec-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="087ec-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="087ec-113">See Also</span></span>

<span data-ttu-id="087ec-114">[**IAgentCharacterEx :: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx :: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="087ec-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




