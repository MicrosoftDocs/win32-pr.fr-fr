---
title: Compréhension des problèmes de mise à l’échelle de l’écran
description: Windows Vista et les versions ultérieures du système d’exploitation permettent aux utilisateurs de modifier le paramètre points par pouce (dpi) pour que la plupart des éléments d’interface utilisateur de l’écran apparaissent plus grands.
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- clients, mise à l’échelle de l’écran UI Automation
- clients, mise à l’échelle de l’écran
- clients, mise à l’échelle
- UI Automation, mise à l’échelle de l’écran
- Automation d’interface utilisateur, mise à l’échelle
- mise à l’échelle de l’écran
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292490"
---
# <a name="understanding-screen-scaling-issues"></a>Compréhension des problèmes de mise à l’échelle de l’écran

Windows Vista et les versions ultérieures du système d’exploitation permettent aux utilisateurs de modifier le paramètre points par pouce (dpi) pour que la plupart des éléments d’interface utilisateur de l’écran apparaissent plus grands. dans les versions antérieures de Windows, la mise à l’échelle devait être implémentée par les applications. dans Windows Vista et versions ultérieures, le Gestionnaire de fenêtrage (DWM) effectue une mise à l’échelle par défaut pour toutes les applications qui ne gèrent pas leur propre mise à l’échelle. Les applications clientes Microsoft UI Automation doivent prendre en compte cette fonctionnalité.

Cette rubrique contient les sections suivantes :

-   [mise à l’échelle dans Windows Vista et versions ultérieures](#scaling-in-windows-vista-and-later)
-   [Mise à l’échelle dans les clients UI Automation](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>mise à l’échelle dans Windows Vista et versions ultérieures

Le paramètre PPP par défaut est 96, ce qui signifie que 96 pixels occupent la largeur ou la hauteur d’un pouce notionnel. La mesure exacte d’un « pouce » dépend de la taille et de la résolution physique du moniteur. Par exemple, sur un moniteur d’une largeur de 12 pouces, pour une résolution horizontale de 1 280 pixels, une ligne horizontale de 96 pixels s’étend sur 9/10e de pouce.

La modification du paramètre PPP n’est pas la même que la modification de la résolution de l’écran. Avec la mise à l’échelle PPP, le nombre de pixels physiques sur l’écran reste le même. Toutefois, la mise à l’échelle est appliquée à la taille et à l’emplacement des éléments d’interface utilisateur. Cette mise à l’échelle peut être effectuée automatiquement par le DWM pour le bureau et pour les applications qui ne demandent pas explicitement à ne pas être mises à l’échelle.

En effet, lorsque l’utilisateur définit le facteur d’échelle sur 120 ppp, un pouce vertical ou horizontal sur l’écran augmente de 25%. Toutes les dimensions sont ajustées en conséquence. Le décalage d’une fenêtre d’application à partir du bord supérieur et du bord gauche de l’écran augmente de 25%. Si la mise à l’échelle de l’application est activée et que l’application n’a pas de prise en charge dpi, la taille de la fenêtre augmente dans la même proportion, avec les décalages et les tailles de tous les éléments d’interface qu’elle contient.

> [!Note]  
> Par défaut, le DWM n’effectue pas de mise à l’échelle pour les applications qui ne prennent pas en charge la résolution lorsque l’utilisateur définit la valeur PPP sur 120, mais effectue une mise à l’échelle lorsque la valeur PPP est définie sur 144 ou une valeur supérieure. Toutefois, l’utilisateur peut remplacer le comportement par défaut.

 

La mise à l’échelle de l’écran pose de nouveaux défis pour les applications qui sont concernées d’une manière ou d’une autre par les coordonnées d’écran. L’écran contient maintenant deux systèmes de coordonnées : l’un physique et l’autre logique. Les coordonnées physiques d’un point correspondent au décalage réel, en pixels, par rapport à l’angle supérieur gauche du point d’origine. Les coordonnées logiques correspondent aux décalages tels qu’ils seraient si les pixels eux-mêmes étaient mis à l’échelle.

Supposons que vous concevez une boîte de dialogue avec un bouton aux coordonnées (100, 48). Lorsque cette boîte de dialogue est affichée avec la valeur par défaut de 96 dpi, le bouton se trouve aux coordonnées physiques de (100, 48). À 120 ppp, il se trouve aux coordonnées physiques de (125, 60). Toutefois, les coordonnées logiques sont les mêmes à n’importe quel paramètre PPP : (100, 48).

Les coordonnées logiques sont importantes, car elles rendent cohérent le comportement du système d’exploitation et des applications, quel que soit le paramètre PPP. Par exemple, en général, la fonction [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) retourne les coordonnées logiques. Si vous déplacez le curseur sur un élément dans une boîte de dialogue, les mêmes coordonnées sont retournées, quel que soit le paramètre PPP. Si vous dessinez un contrôle à l’emplacement (100, 100), il est dessiné à ces coordonnées logiques et occupera la même position relative à n’importe quel paramètre PPP.

## <a name="scaling-in-ui-automation-clients"></a>Mise à l’échelle dans les clients UI Automation

L’API UI Automation n’utilise pas de coordonnées logiques. Les méthodes et propriétés suivantes retournent des coordonnées physiques ou prennent des coordonnées physiques comme paramètres.

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

Par défaut, les applications UI Automation qui s’exécutent dans un environnement qui n’a pas la valeur 96 ppp n’obtiendront pas les résultats corrects à partir de ces méthodes et propriétés. Par exemple, étant donné que la position du curseur est en coordonnées logiques, le client ne peut pas passer ces coordonnées à [**IUIAutomation :: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) pour obtenir l’élément qui se trouve sous le curseur. En outre, l’application n’est pas en mesure de placer correctement les fenêtres en dehors de sa zone cliente.

La solution comporte deux parties.

Tout d’abord, assurez-vous que l’application cliente prend en charge dpi. Pour ce faire, appelez la fonction [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) au démarrage. Cette fonction rend la prise en charge DPI du processus entier, ce qui signifie que toutes les fenêtres qui appartiennent au processus ne sont pas mises à l’échelle.

Deuxièmement, pour connaître les coordonnées du curseur, appelez la fonction [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) .

 

 