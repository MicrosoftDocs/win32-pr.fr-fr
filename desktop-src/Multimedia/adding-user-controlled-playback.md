---
title: Ajout de User-Controlled lecture
description: Ajout de User-Controlled lecture
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511829"
---
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="14075-104">Ajout de User-Controlled lecture</span><span class="sxs-lookup"><span data-stu-id="14075-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="14075-105">Vous pouvez ajouter une lecture contrôlée par l’utilisateur à une application existante en appelant la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) comme suit :</span><span class="sxs-lookup"><span data-stu-id="14075-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="14075-106">Les paramètres [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identifient les descripteurs de la fenêtre parente et de l’instance de module associée à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="14075-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="14075-107">Ils spécifient également les styles de fenêtre et le nom de fichier (ou nom de périphérique) à associer à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="14075-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="14075-108">**MCIWndCreate** effectue automatiquement les étapes suivantes, pour les autres classes de fenêtres, vous devez implémenter vous-même dans votre code :</span><span class="sxs-lookup"><span data-stu-id="14075-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="14075-109">Inscrivez la classe de fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="14075-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="14075-110">Créez la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="14075-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="14075-111">Charge le contenu spécifié.</span><span class="sxs-lookup"><span data-stu-id="14075-111">Load the specified content.</span></span>
4.  <span data-ttu-id="14075-112">Établissez la position de lecture actuelle au début du contenu.</span><span class="sxs-lookup"><span data-stu-id="14075-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="14075-113">Affichez le contrôle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="14075-113">Display the device control.</span></span>
6.  <span data-ttu-id="14075-114">Affichez la zone de lecture de la fenêtre, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="14075-114">Display the playback area of the window, if needed.</span></span>

 

 




