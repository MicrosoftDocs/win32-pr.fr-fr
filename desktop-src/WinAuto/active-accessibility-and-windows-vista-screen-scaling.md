---
title: Mise à l’échelle de l’écran Active Accessibility et Windows Vista
description: Windows Vista permet aux utilisateurs de modifier le paramètre de points par pouce (dpi) pour que la plupart des éléments d’interface utilisateur de l’écran apparaissent plus grands.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db8e192dc01d4c7d75f19741cdfac7b3b08d22c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463479"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Mise à l’échelle de l’écran Active Accessibility et Windows Vista

Windows Vista permet aux utilisateurs de modifier le paramètre de points par pouce (dpi) pour que la plupart des éléments d’interface utilisateur de l’écran apparaissent plus grands. Bien que cette fonctionnalité soit disponible dans Microsoft Windows, dans les versions précédentes, la mise à l’échelle devait être implémentée par les applications. Dans Windows Vista, le Gestionnaire de fenêtrage effectue une mise à l’échelle par défaut pour toutes les applications qui ne gèrent pas leur propre mise à l’échelle. Les applications clientes Microsoft Active Accessibility doivent prendre en compte cette fonctionnalité.

## <a name="scaling-in-windows-vista"></a>Mise à l’échelle dans Windows Vista

Le paramètre PPP par défaut est 96, ce qui signifie que 96 pixels occupent la largeur ou la hauteur d’un pouce notionnel. La mesure exacte d’un « pouce » dépend de la taille et de la résolution physique du moniteur. Par exemple, sur un moniteur d’une largeur de 12 pouces, pour une résolution horizontale de 1 280 pixels, une ligne horizontale de 96 pixels s’étend sur 9/10e de pouce.

La modification du paramètre PPP n’est pas la même que la modification de la résolution de l’écran. Avec la mise à l’échelle PPP, le nombre de pixels physiques sur l’écran reste le même. Toutefois, la mise à l’échelle est appliquée à la taille et à l’emplacement des éléments d’interface utilisateur. Cette mise à l’échelle peut être effectuée automatiquement par le Gestionnaire de fenêtrage (DWM, Desktop Window Manager) pour le bureau et pour les applications qui ne demandent pas explicitement à ne pas être mises à l’échelle.

En effet, lorsque l’utilisateur définit le facteur d’échelle sur 120 ppp, un pouce vertical ou horizontal sur l’écran augmente de 25%. Toutes les dimensions sont ajustées en conséquence. Le décalage d’une fenêtre à partir des bords supérieur et gauche de l’écran augmente de 25%. La taille de la fenêtre augmente dans la même proportion, ainsi que les décalages et les tailles de tous les éléments d’interface utilisateur qu’elle contient.

Par défaut, le DWM n’effectue pas de mise à l’échelle pour les applications qui ne prennent pas en charge DPI lorsque l’utilisateur définit la valeur PPP sur 120, mais l’exécute lorsque la valeur PPP est définie sur une valeur personnalisée 144 ou supérieure. Toutefois, l’utilisateur peut remplacer le comportement par défaut.

La mise à l’échelle de l’écran pose de nouveaux défis pour les applications qui sont concernées d’une manière ou d’une autre par les coordonnées d’écran. L’écran contient maintenant deux systèmes de coordonnées : l’un physique et l’autre logique. Les coordonnées physiques d’un point correspondent au décalage réel en pixels par rapport au point d’origine en haut à gauche. Les coordonnées logiques correspondent aux décalages tels qu’ils seraient si les pixels eux-mêmes étaient mis à l’échelle.

Supposons que vous concevez une boîte de dialogue avec un bouton aux coordonnées (100, 48). Lorsque cette boîte de dialogue est affichée avec la valeur par défaut de 96 dpi, le bouton se trouve aux coordonnées physiques de (100, 48). À 120 ppp, il se trouve aux coordonnées physiques de (125, 60). Toutefois, les coordonnées logiques sont les mêmes à n’importe quel paramètre PPP : (100, 48).

Les coordonnées logiques sont importantes, car elles rendent cohérent le comportement du système d’exploitation et des applications quel que soit le paramètre PPP. Par exemple, **System. Windows. Forms. Cursor. position** retourne normalement les coordonnées logiques. Si vous déplacez le curseur sur un élément dans une boîte de dialogue, les mêmes coordonnées sont retournées quel que soit le paramètre PPP. Si vous dessinez un contrôle à l’emplacement (100, 100), il est dessiné à ces coordonnées logiques et occupera la même position relative à n’importe quel paramètre PPP.

## <a name="scaling-in-active-accessibility-clients"></a>Mise à l’échelle dans les clients Active Accessibility

Microsoft Active Accessibility n’utilise pas de coordonnées logiques. Les méthodes et les fonctions suivantes retournent des coordonnées physiques ou les prennent comme paramètres.

-   [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

Par défaut, une application cliente Microsoft Active Accessibility s’exécutant dans un environnement qui n’est pas 96 ppp ne peut pas obtenir les résultats corrects à partir de ces appels. Par exemple, étant donné que la position du curseur est en coordonnées logiques, le client ne peut pas simplement passer ces coordonnées à [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) pour obtenir l’élément qui se trouve sous le curseur.

En outre, une application qui crée une fenêtre en dehors de sa zone cliente, telle qu’une application d’accessibilité qui met en évidence des éléments d’interface utilisateur ciblés, ne crée pas la fenêtre à l’emplacement d’écran approprié, car la fenêtre est placée aux coordonnées logiques, et non pas aux coordonnées physiques retournées par [**IAccessible :: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

La solution est en deux parties :

-   Rendre l’application cliente prise en charge dpi. Pour ce faire, appelez la fonction [**SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) au démarrage. Cette fonction rend la prise en charge DPI du processus entier, ce qui signifie que toutes les fenêtres qui appartiennent au processus ne sont pas mises à l’échelle.
-   Utilisez des fonctions compatibles dpi. Par exemple, pour obtenir les coordonnées du curseur, appelez la fonction [**GetPhysicalCursorPos**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) . N’utilisez pas [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); son comportement dans les applications prenant en charge DPI n’est pas défini.

Si votre application effectue une communication interprocessus directe avec des applications qui ne prennent pas en charge dpi, vous pouvez effectuer une conversion entre les coordonnées logiques et physiques à l’aide des fonctions [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) et [**LogicalToPhysicalPoint**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) .

 

 