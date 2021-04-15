---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463115"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="55739-103">IAgentEx::ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="55739-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="55739-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="55739-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="55739-105">Affiche la fenêtre Propriétés des caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="55739-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="55739-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="55739-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="55739-107"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="55739-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="55739-108">Coordonnée x de la fenêtre, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="55739-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="55739-109"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="55739-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="55739-110">Coordonnée y de la fenêtre, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="55739-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="55739-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span><span class="sxs-lookup"><span data-stu-id="55739-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="55739-112">Indicateur de position par défaut.</span><span class="sxs-lookup"><span data-stu-id="55739-112">Default position flag.</span></span> <span data-ttu-id="55739-113">Si ce paramètre a la **valeur true**, Microsoft Agent affiche la fenêtre de la feuille de propriétés pour le caractère par défaut au dernier emplacement.</span><span class="sxs-lookup"><span data-stu-id="55739-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="55739-114">Pour Windows 2000, il peut être nécessaire d’appeler la nouvelle API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) pour vous assurer que cette fenêtre devient la fenêtre de premier plan.</span><span class="sxs-lookup"><span data-stu-id="55739-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="55739-115">Pour plus d’informations sur la définition de la fenêtre de premier plan sous Windows 2000, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="55739-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="55739-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55739-116">See Also</span></span>

[<span data-ttu-id="55739-117">**IAgentNotifySinkEx ::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="55739-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 