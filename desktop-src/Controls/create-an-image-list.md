---
title: Comment créer une liste d’images
description: Cette rubrique montre comment utiliser la fonction ImageList \_ Create pour créer une liste d’images.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c81ff3a46138c210474a1b00ddd2ba647d1368
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941491"
---
# <a name="how-to-create-an-image-list"></a>Comment créer une liste d’images

Cette rubrique montre comment utiliser la fonction [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) pour créer une liste d’images.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Pour créer une liste d’images, appelez la fonction [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . Les paramètres incluent le type de liste d’images à créer, les dimensions de chaque image et le nombre d’images que vous avez l’intention d’ajouter à la liste.

L’exemple suivant crée une liste d’images masquées et utilise la macro [**ImageList \_ addicon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) pour ajouter deux icônes à la liste.



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les listes d’images](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[À propos des listes d’images](image-lists.md)
</dt> <dt>

[Utilisation de listes d’images](using-image-lists.md)
</dt> </dl>

 

 




