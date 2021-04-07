---
title: Implémentation de CPluginWindow
description: Implémentation de CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Plug-ins du lecteur Windows Media, classe CPluginWindow
- plug-ins, classe CPluginWindow
- plug-ins d’interface utilisateur, classe CPluginWindow
- Plug-ins d’interface utilisateur, classe CPluginWindow
- CPluginWindow, classe
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672249"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="184f5-109">Implémentation de CPluginWindow</span><span class="sxs-lookup"><span data-stu-id="184f5-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="184f5-110">La classe CPluginWindow fournit l’interface utilisateur du plug-in.</span><span class="sxs-lookup"><span data-stu-id="184f5-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="184f5-111">Dans le cas du plug-in de l’interface utilisateur de recherche, cette classe contient le code pour le bouton **Rechercher** et le code qui lance la page de recherche lorsque l’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="184f5-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="184f5-112">L’Assistant fournit une implémentation de base de CPluginWindow dans le fichier d’en-tête CPluginWindow. h.</span><span class="sxs-lookup"><span data-stu-id="184f5-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="184f5-113">Pour simplifier les choses, le plug-in de l’interface utilisateur de recherche modifie ce fichier directement, bien que les ajouts approfondis soient normalement placés dans un fichier CPluginWindow. cpp distinct.</span><span class="sxs-lookup"><span data-stu-id="184f5-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="184f5-114">Les sections suivantes décrivent ce que vous devez faire pour implémenter CPluginWindow :</span><span class="sxs-lookup"><span data-stu-id="184f5-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="184f5-115">La table des messages</span><span class="sxs-lookup"><span data-stu-id="184f5-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="184f5-116">Le constructeur</span><span class="sxs-lookup"><span data-stu-id="184f5-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="184f5-117">Méthode OnPaint</span><span class="sxs-lookup"><span data-stu-id="184f5-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="184f5-118">La méthode OnCreate</span><span class="sxs-lookup"><span data-stu-id="184f5-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="184f5-119">Méthode OnSearch</span><span class="sxs-lookup"><span data-stu-id="184f5-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="184f5-120">Méthode LaunchPage</span><span class="sxs-lookup"><span data-stu-id="184f5-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="184f5-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="184f5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="184f5-122">**Guide de programmation de plug-ins d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="184f5-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




