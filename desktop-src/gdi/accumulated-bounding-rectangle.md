---
description: Le rectangle englobant cumulé est le plus petit rectangle englobant la partie d’une fenêtre ou d’une zone client affectée par les opérations de dessin récentes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rectangle englobant cumulé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528401"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="75e69-103">Rectangle englobant cumulé</span><span class="sxs-lookup"><span data-stu-id="75e69-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="75e69-104">Le *rectangle englobant cumulé* est le plus petit rectangle englobant la partie d’une fenêtre ou d’une zone client affectée par les opérations de dessin récentes.</span><span class="sxs-lookup"><span data-stu-id="75e69-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="75e69-105">Une application peut utiliser ce rectangle pour déterminer facilement l’étendue des modifications provoquées par les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="75e69-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="75e69-106">Il est parfois utilisé conjointement avec [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) pour déterminer la partie de la zone cliente qui doit être redessinée après l’effacement du verrou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="75e69-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="75e69-107">Une application utilise la fonction [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (en spécifiant l' \_ activation de DCB) pour commencer à accumuler le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="75e69-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="75e69-108">Le système accumule ensuite les points pour le rectangle englobant lorsque l’application utilise le contexte de périphérique d’affichage spécifié.</span><span class="sxs-lookup"><span data-stu-id="75e69-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="75e69-109">L’application peut récupérer le rectangle englobant actuel à tout moment à l’aide de la fonction [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) .</span><span class="sxs-lookup"><span data-stu-id="75e69-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="75e69-110">L’application arrête l’accumulation en appelant à nouveau **SetBoundsRect** , en spécifiant la \_ valeur de désactivation de DCB.</span><span class="sxs-lookup"><span data-stu-id="75e69-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



