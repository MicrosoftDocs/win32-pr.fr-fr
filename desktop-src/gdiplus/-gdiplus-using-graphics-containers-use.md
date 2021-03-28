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
# <a name="using-graphics-containers"></a>Utilisation de conteneurs graphiques

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit des méthodes telles que [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))et [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) pour afficher des images vectorielles, des images raster et du texte. Un objet **Graphics** a également plusieurs propriétés qui influencent la qualité et l’orientation des éléments dessinés. Par exemple, la propriété mode de lissage détermine si l’anticrénelage est appliqué aux lignes et aux courbes, et la propriété de transformation universelle influence la position et la rotation des éléments qui sont dessinés.

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est souvent associé à un périphérique d’affichage particulier. Lorsque vous utilisez un objet **Graphics** pour dessiner dans une fenêtre, l’objet **Graphics** est également associé à cette fenêtre particulière.

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) peut être considéré comme un conteneur, car il contient un ensemble de propriétés qui influencent le dessin, et il est lié à des informations spécifiques à l’appareil. Vous pouvez créer un conteneur secondaire dans un objet **Graphics** existant en appelant la méthode [BeginContainer](/previous-versions//ms535731(v=vs.85)) de cet objet **Graphics** .

Les rubriques suivantes décrivent plus en détail les objets [**graphiques**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et les conteneurs imbriqués :

-   [État d’un objet Graphics](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Conteneurs Graphics imbriqués](-gdiplus-nested-graphics-containers-use.md)

 

 
