---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840362"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="23aba-103">IAgentCharacterEx::ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="23aba-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="23aba-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="23aba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="23aba-105">Affiche le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="23aba-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="23aba-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="23aba-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="23aba-107"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="23aba-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="23aba-108">Coordonnée x du menu contextuel du caractère, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="23aba-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="23aba-109"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="23aba-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="23aba-110">Coordonnée y du menu contextuel du caractère, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="23aba-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="23aba-111">Lorsque vous affectez à [**IAgentCharacterEx :: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) la **valeur false**, le serveur n’affiche plus automatiquement le menu lorsque vous cliquez avec le bouton droit sur le caractère ou sur son icône de barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="23aba-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="23aba-112">Vous pouvez utiliser cette méthode pour afficher le menu.</span><span class="sxs-lookup"><span data-stu-id="23aba-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="23aba-113">Le menu s’affiche jusqu’à ce que l’utilisateur sélectionne une commande ou affiche un autre menu.</span><span class="sxs-lookup"><span data-stu-id="23aba-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="23aba-114">Un seul menu contextuel peut être affiché à la fois ; par conséquent, les appels à cette méthode annulent (supprime) le menu précédent.</span><span class="sxs-lookup"><span data-stu-id="23aba-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="23aba-115">Cette méthode ne doit être appelée que lorsque votre application cliente est le client actif du caractère ; dans le cas contraire, elle échoue.</span><span class="sxs-lookup"><span data-stu-id="23aba-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="23aba-116">**IAgentCharacterEx::SetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="23aba-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 




