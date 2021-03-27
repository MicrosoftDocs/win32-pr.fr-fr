---
description: Le système réduit la fenêtre principale d’une application (style chevauchant) à une fenêtre réduite lorsque l’utilisateur clique sur réduire dans le menu fenêtre ou l’application appelle la fonction ShowWindow et spécifie une valeur telle que SW \_ Minimize.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Fenêtres réduites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754380"
---
# <a name="minimized-windows"></a><span data-ttu-id="c01f3-103">Fenêtres réduites</span><span class="sxs-lookup"><span data-stu-id="c01f3-103">Minimized Windows</span></span>

<span data-ttu-id="c01f3-104">Le système réduit la fenêtre principale d’une application (style chevauchant) à une fenêtre réduite lorsque l’utilisateur clique sur réduire dans le menu fenêtre ou l’application appelle la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) et spécifie une valeur telle que SW \_ Minimize.</span><span class="sxs-lookup"><span data-stu-id="c01f3-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="c01f3-105">La réduction d’une fenêtre accélère les performances du système en réduisant la quantité de travail qu’une application doit effectuer lors de la mise à jour de sa fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="c01f3-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="c01f3-106">Pour une application classique, le système dessine une icône, appelée icône de classe, lorsque la fenêtre est réduite, en l’étiquetant avec le nom de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c01f3-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="c01f3-107">L’icône de classe, une image statique qui représente l’application, est spécifiée par l’application lors de l’inscription de la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c01f3-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="c01f3-108">L’application assigne un handle à l’icône de classe au membre **HICON** de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) avant d’appeler [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="c01f3-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="c01f3-109">L’application peut utiliser la fonction [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) pour récupérer le handle d’icône.</span><span class="sxs-lookup"><span data-stu-id="c01f3-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
