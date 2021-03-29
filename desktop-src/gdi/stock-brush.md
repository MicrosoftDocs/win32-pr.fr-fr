---
description: Il existe sept pinceaux de stock logique prédéfinis gérés par l’interface GDI (Graphics Device Interface). Il y a également 21 pinceaux de stock logique prédéfinis gérés par l’interface de gestion de fenêtre (utilisateur).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pinceau boursier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973635"
---
# <a name="stock-brush"></a><span data-ttu-id="0dc08-104">Pinceau boursier</span><span class="sxs-lookup"><span data-stu-id="0dc08-104">Stock Brush</span></span>

<span data-ttu-id="0dc08-105">Il existe sept pinceaux de stock logique prédéfinis gérés par l’interface GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="0dc08-105">There are seven predefined logical stock brushes maintained by the graphics device interface (GDI).</span></span> <span data-ttu-id="0dc08-106">Il y a également 21 pinceaux de stock logique prédéfinis gérés par l’interface de gestion de fenêtre (utilisateur).</span><span class="sxs-lookup"><span data-stu-id="0dc08-106">There are also 21 predefined logical stock brushes maintained by the window management interface (USER).</span></span>

<span data-ttu-id="0dc08-107">L’illustration suivante montre des rectangles peints à l’aide des sept pinceaux boursiers prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="0dc08-107">The following illustration shows rectangles painted by using the seven predefined stock brushes.</span></span>

![Illustration montrant sept boîtes : un noir, trois nuances de gris et trois qui apparaissent vides](images/csbru-03.png)

<span data-ttu-id="0dc08-109">Une application peut récupérer un handle identifiant l’un des sept pinceaux boursiers en appelant la fonction [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , en spécifiant le type de pinceau.</span><span class="sxs-lookup"><span data-stu-id="0dc08-109">An application can retrieve a handle identifying one of the seven stock brushes by calling the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function, specifying the brush type.</span></span>

<span data-ttu-id="0dc08-110">Les 21 actions boursières gérées par l’interface de gestion des fenêtres correspondent aux couleurs des éléments de la fenêtre, tels que les menus, les barres de défilement et les boutons.</span><span class="sxs-lookup"><span data-stu-id="0dc08-110">The 21 stock brushes maintained by the window management interface correspond to the colors of window elements such as menus, scroll bars, and buttons.</span></span> <span data-ttu-id="0dc08-111">Une application peut obtenir un handle identifiant l’un de ces pinceaux en appelant la fonction [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) et en spécifiant une valeur de couleur système.</span><span class="sxs-lookup"><span data-stu-id="0dc08-111">An application can obtain a handle identifying one of these brushes by calling the [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) function and specifying a system-color value.</span></span> <span data-ttu-id="0dc08-112">Une application peut récupérer la couleur correspondant à un élément de fenêtre particulier en appelant la fonction [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) .</span><span class="sxs-lookup"><span data-stu-id="0dc08-112">An application can retrieve the color corresponding to a particular window element by calling the [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) function.</span></span> <span data-ttu-id="0dc08-113">Une application peut définir la couleur correspondant à un élément de fenêtre en appelant la fonction [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="0dc08-113">An application can set the color corresponding to a window element by calling the [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) function.</span></span>

 

 
