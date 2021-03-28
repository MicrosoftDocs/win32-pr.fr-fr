---
description: Les fonctions suivantes assurent la prise en charge de plusieurs analyses.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Fonctions d’analyse de plusieurs affichages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972639"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="30117-103">Fonctions d’analyse de plusieurs affichages</span><span class="sxs-lookup"><span data-stu-id="30117-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="30117-104">Les fonctions suivantes assurent la prise en charge de plusieurs analyses.</span><span class="sxs-lookup"><span data-stu-id="30117-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="30117-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="30117-105">Function</span></span>                                           | <span data-ttu-id="30117-106">Description</span><span class="sxs-lookup"><span data-stu-id="30117-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30117-107">**EnumDisplayMonitors**</span><span class="sxs-lookup"><span data-stu-id="30117-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="30117-108">Énumère les moniteurs d’affichage qui croisent une région formée par l’intersection d’un rectangle de découpage spécifié et la région visible d’un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="30117-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="30117-109">**GetMonitorInfo**</span><span class="sxs-lookup"><span data-stu-id="30117-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="30117-110">Récupère des informations sur un moniteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="30117-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="30117-111">**MonitorEnumProc**</span><span class="sxs-lookup"><span data-stu-id="30117-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="30117-112">Fonction de rappel définie par l’application qui est appelée par la fonction [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="30117-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="30117-113">**MonitorFromPoint**</span><span class="sxs-lookup"><span data-stu-id="30117-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="30117-114">Récupère un handle vers l’écran d’affichage qui contient un point spécifié.</span><span class="sxs-lookup"><span data-stu-id="30117-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="30117-115">**MonitorFromRect**</span><span class="sxs-lookup"><span data-stu-id="30117-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="30117-116">Récupère un handle vers le moniteur d’affichage qui a la plus grande zone d’intersection avec un rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="30117-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="30117-117">**MonitorFromWindow**</span><span class="sxs-lookup"><span data-stu-id="30117-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="30117-118">Récupère un handle vers l’écran d’affichage qui a la plus grande zone d’intersection avec le rectangle englobant d’une fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="30117-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



