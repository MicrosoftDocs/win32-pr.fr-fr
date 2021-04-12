---
title: STYLE (instruction)
description: Définit le style de la fenêtre de la boîte de dialogue. Le style de fenêtre spécifie si la zone est une fenêtre contextuelle ou une fenêtre enfant.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menus de l’instruction de STYLE et autres ressources
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381895"
---
# <a name="style-statement"></a><span data-ttu-id="8b36f-105">STYLE (instruction)</span><span class="sxs-lookup"><span data-stu-id="8b36f-105">STYLE statement</span></span>

<span data-ttu-id="8b36f-106">Définit le style de la fenêtre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8b36f-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="8b36f-107">Le style de fenêtre spécifie si la zone est une fenêtre contextuelle ou une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="8b36f-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="8b36f-108"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="8b36f-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="8b36f-109">Style de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8b36f-109">The window style.</span></span> <span data-ttu-id="8b36f-110">Ce paramètre peut être une valeur entière ou une combinaison de valeurs de style de fenêtre (par exemple, **WS \_ Caption** et **WS \_ SYSMENU**) et des valeurs de style de boîte de dialogue (par exemple, **DS \_ Center**).</span><span class="sxs-lookup"><span data-stu-id="8b36f-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="8b36f-111">Pour obtenir la liste des styles de fenêtre, consultez [styles de fenêtre](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="8b36f-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="8b36f-112">Pour obtenir la liste des styles de boîte de dialogue, consultez [styles de modèle](../dlgbox/about-dialog-boxes.md)de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8b36f-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="8b36f-113">Si vous utilisez les valeurs de style de la fenêtre ou de la boîte de dialogue, vous devez inclure Windows. h.</span><span class="sxs-lookup"><span data-stu-id="8b36f-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 