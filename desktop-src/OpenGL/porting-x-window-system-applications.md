---
title: Portage des applications du système de fenêtre X
description: Portage des applications du système de fenêtre X
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL sur Windows, Portage
- portage vers OpenGL, système de fenêtre X
- Portage OpenGL, système X Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196871"
---
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="16a3f-106">Portage des applications du système de fenêtre X</span><span class="sxs-lookup"><span data-stu-id="16a3f-106">Porting X Window System Applications</span></span>

<span data-ttu-id="16a3f-107">Comme Windows, le système de fenêtre X est un système de gestion d’événements et de message qui utilise des menus et des contrôles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="16a3f-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="16a3f-108">Le code OpenGL de votre application système X Window est probablement situé dans des zones qui correspondent approximativement à l’emplacement où il apparaîtra lorsque vous le portagerez vers Windows.</span><span class="sxs-lookup"><span data-stu-id="16a3f-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="16a3f-109">La majeure partie de votre code OpenGL ne changera pas, mais vous devez réécrire le code qui est spécifique au système X Window.</span><span class="sxs-lookup"><span data-stu-id="16a3f-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="16a3f-110">**Utilisez la procédure générale suivante pour porter les programmes OpenGL du système X Window vers Windows**</span><span class="sxs-lookup"><span data-stu-id="16a3f-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="16a3f-111">Réécrivez le code spécifique au système X Window à l’aide d’un code Windows équivalent.</span><span class="sxs-lookup"><span data-stu-id="16a3f-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="16a3f-112">Recherchez le code de création de fenêtre et de gestion d’événements.</span><span class="sxs-lookup"><span data-stu-id="16a3f-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="16a3f-113">Le système de fenêtres X et les fenêtres sont des systèmes de gestion d’événements et de fenêtrage basés sur les messages, ce qui facilite la détermination de l’emplacement des modifications appropriées.</span><span class="sxs-lookup"><span data-stu-id="16a3f-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="16a3f-114">(Toutefois, en particulier pour les applications volumineuses, la réécriture d’une application d’un système d’exploitation à un autre peut être une entreprise complexe et difficile.)</span><span class="sxs-lookup"><span data-stu-id="16a3f-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="16a3f-115">Localisez tout code qui utilise des fonctions GLX.</span><span class="sxs-lookup"><span data-stu-id="16a3f-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="16a3f-116">Il s’agit des fonctions que vous allez traduire en leurs fonctions Windows équivalentes.</span><span class="sxs-lookup"><span data-stu-id="16a3f-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="16a3f-117">Traduisez les fonctions de format de pixel GLX et les fonctions visuelles/Dessinables au format de pixel Windows/OpenGL approprié et aux fonctions de contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="16a3f-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="16a3f-118">Traduisez les fonctions de contexte de rendu GLX en fonctions de contexte de rendu Windows/OpenGL.</span><span class="sxs-lookup"><span data-stu-id="16a3f-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="16a3f-119">Traduisez les fonctions GLX pixmap en fonctions Windows équivalentes.</span><span class="sxs-lookup"><span data-stu-id="16a3f-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="16a3f-120">Traduisez GLX trame et d’autres fonctions GLX en fonctions Windows appropriées.</span><span class="sxs-lookup"><span data-stu-id="16a3f-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




