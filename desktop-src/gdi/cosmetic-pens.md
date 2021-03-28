---
description: Les dimensions d’un stylet cosmétique sont spécifiées en unités de périphérique.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Plumes cosmétiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754468"
---
# <a name="cosmetic-pens"></a><span data-ttu-id="5cab1-103">Plumes cosmétiques</span><span class="sxs-lookup"><span data-stu-id="5cab1-103">Cosmetic Pens</span></span>

<span data-ttu-id="5cab1-104">Les dimensions d’un stylet cosmétique sont spécifiées en unités de périphérique.</span><span class="sxs-lookup"><span data-stu-id="5cab1-104">The dimensions of a cosmetic pen are specified in device units.</span></span> <span data-ttu-id="5cab1-105">Par conséquent, les lignes dessinées avec un stylet cosmétique ont toujours une largeur fixe.</span><span class="sxs-lookup"><span data-stu-id="5cab1-105">Therefore, lines drawn with a cosmetic pen always have a fixed width.</span></span> <span data-ttu-id="5cab1-106">Les lignes dessinées avec un stylet cosmétique sont généralement tracées 3 à 10 fois plus rapidement que les lignes dessinées avec un stylet géométrique.</span><span class="sxs-lookup"><span data-stu-id="5cab1-106">Lines drawn with a cosmetic pen are generally drawn 3 to 10 times faster than lines drawn with a geometric pen.</span></span> <span data-ttu-id="5cab1-107">Les plumes cosmétiques ont trois attributs : la largeur, le style et la couleur.</span><span class="sxs-lookup"><span data-stu-id="5cab1-107">Cosmetic pens have three attributes: width, style, and color.</span></span> <span data-ttu-id="5cab1-108">Pour plus d’informations sur ces attributs, consultez [Pen Attributes](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="5cab1-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="5cab1-109">Pour créer un stylet cosmétique, utilisez la fonction [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="5cab1-109">To create a cosmetic pen, use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="5cab1-110">Pour récupérer l’un des trois plumes cosmétiques de l’action géré par le système, utilisez la fonction [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="5cab1-110">To retrieve one of the three stock cosmetic pens managed by the system, use the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function.</span></span>

<span data-ttu-id="5cab1-111">Une fois que vous avez créé un stylet (ou obtenu un handle vers l’un des plumes d’inventaire), sélectionnez le stylet dans le contexte de périphérique (DC) de l’application à l’aide de la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="5cab1-111">After you create a pen (or obtain a handle to one of the stock pens), select the pen into the application's device context (DC) using the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="5cab1-112">À partir de ce point, l’application utilise ce stylet pour toutes les opérations de dessin de lignes dans sa zone cliente.</span><span class="sxs-lookup"><span data-stu-id="5cab1-112">From this point on, the application uses this pen for any line-drawing operations in its client area.</span></span>

 

 



