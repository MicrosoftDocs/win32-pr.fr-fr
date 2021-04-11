---
description: 'Les applications Direct3D peuvent s’exécuter dans l’un ou l’autre des deux modes : plein écran ou fenêtre.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Mode fenêtre/Full-Screen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108734"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="fc5cb-103">Mode fenêtre/Full-Screen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fc5cb-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="fc5cb-104">Les applications Direct3D peuvent s’exécuter dans l’un ou l’autre des deux modes : plein écran ou fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="fc5cb-105">Le mode plein écran signifie que la fenêtre dans laquelle l’application s’exécute couvre l’ensemble du bureau, en masquant toutes les applications en cours d’exécution (y compris votre environnement de développement).</span><span class="sxs-lookup"><span data-stu-id="fc5cb-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="fc5cb-106">Les jeux utilisent généralement le mode plein écran par défaut pour plonger entièrement l’utilisateur dans le jeu en masquant toutes les applications en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="fc5cb-107">Une application exécutée en mode fenêtre partage le bureau avec toutes les applications en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="fc5cb-108">Les différences de code entre le mode plein écran et le mode fenêtre sont très petites.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="fc5cb-109">Étant donné qu’une application s’exécutant en mode plein écran prend le contrôle à l’écran, le débogage de l’application nécessite un moniteur distinct ou l’utilisation d’un débogueur distant.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="fc5cb-110">Utilisez l' [outil panneau de configuration DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) pour activer le débogage à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="fc5cb-111">L’un des avantages d’une application en mode fenêtre est que vous pouvez effectuer un pas à pas détaillé dans le code d’un débogueur sans plusieurs analyses ou un débogueur distant.</span><span class="sxs-lookup"><span data-stu-id="fc5cb-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc5cb-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc5cb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc5cb-113">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="fc5cb-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



