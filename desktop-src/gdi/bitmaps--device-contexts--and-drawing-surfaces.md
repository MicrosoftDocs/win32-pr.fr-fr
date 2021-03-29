---
description: Un contexte de périphérique (DC) est une structure de données qui définit les objets graphiques, leurs attributs associés et les modes graphiques qui affectent la sortie sur un appareil. Pour créer un contrôleur de périphérique, appelez la fonction CreateDC ; pour récupérer un contrôleur de périphérique, appelez la fonction GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Images bitmap, contextes de périphérique et surfaces de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202054"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="6185d-104">Images bitmap, contextes de périphérique et surfaces de dessin</span><span class="sxs-lookup"><span data-stu-id="6185d-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="6185d-105">Un *contexte de périphérique* (DC) est une structure de données qui définit les objets graphiques, leurs attributs associés et les modes graphiques qui affectent la sortie sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="6185d-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="6185d-106">Pour créer un contrôleur de périphérique, appelez la fonction [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ; pour récupérer un contrôleur de périphérique, appelez la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="6185d-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="6185d-107">Avant de retourner un descripteur qui identifie ce contrôleur de réseau, le système sélectionne une surface de dessin dans le contrôleur de réseau.</span><span class="sxs-lookup"><span data-stu-id="6185d-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="6185d-108">Si l’application a appelé la fonction [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) pour créer un contexte de périphérique pour un affichage VGA, les dimensions de cette surface de dessin sont de 640 x 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="6185d-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="6185d-109">Si l’application a appelé la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , les dimensions reflètent la taille de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="6185d-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="6185d-110">Avant qu’une application puisse commencer à dessiner, elle doit sélectionner une image bitmap avec la largeur et la hauteur appropriées dans le DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="6185d-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="6185d-111">Quand une application transmet le descripteur au contrôleur de l’une des fonctions de dessin GDI (Graphics Device Interface), la sortie demandée apparaît sur la surface de dessin sélectionnée dans le contrôleur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6185d-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="6185d-112">Pour plus d’informations, consultez [contextes de périphérique mémoire](memory-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="6185d-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



