---
title: Utilisation d’une interface multidocument
description: Utilisation d’une interface multidocument
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc30d177ee7b0dd8ae0c5d9ca23c5d6ca577c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842229"
---
# <a name="using-a-multiple-document-interface"></a><span data-ttu-id="4f934-104">Utilisation d’une interface multidocument</span><span class="sxs-lookup"><span data-stu-id="4f934-104">Using a Multiple Document Interface</span></span>

<span data-ttu-id="4f934-105">Les applications qui utilisent une interface multidocument (MDI) peuvent avoir besoin de spécifier des styles de fenêtre qui ne sont pas disponibles via la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="4f934-105">Applications that use a multiple document interface (MDI) might need to specify window styles that are not available through the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="4f934-106">Pour ces applications, vous pouvez inscrire et créer une fenêtre MCIWnd à l’aide de la fonction [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) avec la fonction [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="4f934-106">For these applications, you can register and create an MCIWnd window by using the [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) function with the [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="4f934-107">La fonction **MCIWndRegisterClass** enregistre la \_ \_ classe de fenêtre de la classe de fenêtre MCIWND, puis **CreateWindowEx** crée une instance d’une fenêtre MCIWND.</span><span class="sxs-lookup"><span data-stu-id="4f934-107">The **MCIWndRegisterClass** function registers the MCIWND\_WINDOW\_CLASS window class and then **CreateWindowEx** creates an instance of an MCIWnd window.</span></span>

 

 