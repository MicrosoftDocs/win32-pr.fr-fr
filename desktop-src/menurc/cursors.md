---
title: Curseurs
description: Cette section décrit les curseurs qui sont de petites images dont l’emplacement sur l’écran est contrôlé par un dispositif de pointage, tel qu’une souris, un stylet ou un Trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- ressources, curseurs
- curseurs, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7be5b8e213dd1911d2227a3dce4b61078ab1a22711d4e765525c7fbd5bd08d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712609"
---
# <a name="cursors"></a>Curseurs

Un curseur est une petite image dont l’emplacement sur l’écran est contrôlé par un dispositif de pointage, tel qu’une souris, un stylet ou un Trackball. Dans le reste de cette vue d’ensemble, le terme Mouse fait référence à n’importe quel dispositif de pointage.

Lorsque l’utilisateur déplace la souris, le système déplace le curseur en conséquence. Les fonctions de curseur permettent aux applications de créer, charger, afficher, animer, déplacer, restreindre et détruire des curseurs.

### <a name="in-this-section"></a>Dans cette section



| Name                                     | Description                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [À propos des curseurs](about-cursors.md)       | Décrit les curseurs standard.<br/>                    |
| [Utilisation de curseurs](using-cursors.md)       | Explique comment effectuer des tâches liées aux curseurs.<br/> |
| [Référence du curseur](cursor-reference.md) | Contient la référence de l’API.<br/>                        |



 

### <a name="cursor-functions"></a>Fonctions de curseur



| Name                                                 | Description                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Permet d’affiner le curseur sur une zone rectangulaire de l’écran. Si une position de curseur suivante (définie par la fonction [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) ou la souris) se trouve en dehors du rectangle, le système ajuste automatiquement la position pour maintenir le curseur à l’intérieur de la zone rectangulaire. <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Copie le curseur spécifié. <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Crée un curseur avec la taille, les modèles de bits et la zone réactive spécifiés. <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Détruit un curseur et libère la mémoire occupée par le curseur. N’utilisez pas cette fonction pour détruire un curseur partagé.<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Récupère les coordonnées d’écran de la zone rectangulaire à laquelle le curseur est confiné. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Récupère un handle vers le curseur actuel. <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Récupère des informations sur le curseur global.<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Récupère la position du curseur, en coordonnées d’écran.<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Récupère la position du curseur en coordonnées physiques.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Charge la ressource de curseur spécifiée à partir du fichier exécutable (.EXE) associé à une instance d’application.<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Crée un curseur en fonction des données contenues dans un fichier. <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Définit la forme du curseur. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Déplace le curseur vers les coordonnées d’écran spécifiées. Si les nouvelles coordonnées ne se trouvent pas dans le rectangle d’écran défini par l’appel de fonction [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) le plus récent, le système ajuste automatiquement les coordonnées afin que le curseur reste dans le rectangle. <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Définit la position du curseur en coordonnées physiques.<br/>                                                                                                                                                                                                                                    |
| [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Permet à une application de personnaliser les curseurs système. Elle remplace le contenu du curseur système spécifié par le paramètre *ID* par le contenu du curseur spécifié par le paramètre *hcur* , puis détruit *hcur*. <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Affiche ou masque le curseur. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Notifications de curseur



| Name                                  | Description                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_SETCURSOR WM**](wm-setcursor.md) | Envoyé à une fenêtre si la souris provoque le déplacement du curseur dans une fenêtre et que l’entrée de la souris n’est pas capturée. <br/> |



 

### <a name="cursor-structures"></a>Structures de curseur



| Name                             | Description                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Contient des informations de curseur globales.<br/> |



 

 

 





