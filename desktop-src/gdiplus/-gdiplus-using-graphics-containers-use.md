---
description: Un objet Graphics fournit des méthodes telles que DrawLine, DrawImage et DrawString pour afficher des images vectorielles, des images raster et du texte.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilisation de conteneurs graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972826"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="8a278-103">Utilisation de conteneurs graphiques</span><span class="sxs-lookup"><span data-stu-id="8a278-103">Using Graphics Containers</span></span>

<span data-ttu-id="8a278-104">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit des méthodes telles que [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))et [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) pour afficher des images vectorielles, des images raster et du texte.</span><span class="sxs-lookup"><span data-stu-id="8a278-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="8a278-105">Un objet **Graphics** a également plusieurs propriétés qui influencent la qualité et l’orientation des éléments dessinés.</span><span class="sxs-lookup"><span data-stu-id="8a278-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="8a278-106">Par exemple, la propriété mode de lissage détermine si l’anticrénelage est appliqué aux lignes et aux courbes, et la propriété de transformation universelle influence la position et la rotation des éléments qui sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="8a278-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="8a278-107">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est souvent associé à un périphérique d’affichage particulier.</span><span class="sxs-lookup"><span data-stu-id="8a278-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="8a278-108">Lorsque vous utilisez un objet **Graphics** pour dessiner dans une fenêtre, l’objet **Graphics** est également associé à cette fenêtre particulière.</span><span class="sxs-lookup"><span data-stu-id="8a278-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="8a278-109">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) peut être considéré comme un conteneur, car il contient un ensemble de propriétés qui influencent le dessin, et il est lié à des informations spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8a278-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="8a278-110">Vous pouvez créer un conteneur secondaire dans un objet **Graphics** existant en appelant la méthode [BeginContainer](/previous-versions//ms535731(v=vs.85)) de cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="8a278-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="8a278-111">Les rubriques suivantes décrivent plus en détail les objets [**graphiques**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et les conteneurs imbriqués :</span><span class="sxs-lookup"><span data-stu-id="8a278-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="8a278-112">État d’un objet Graphics</span><span class="sxs-lookup"><span data-stu-id="8a278-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="8a278-113">Conteneurs Graphics imbriqués</span><span class="sxs-lookup"><span data-stu-id="8a278-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
