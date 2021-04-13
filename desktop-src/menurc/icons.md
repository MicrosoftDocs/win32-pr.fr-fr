---
title: Icônes (menus et autres ressources)
description: Cette section décrit les icônes qui sont des images bitmap associées à un masque pour créer des zones transparentes dans l’image.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\icons.htm
keywords:
- ressources, icônes
- icônes, à propos de
- Ressource RT_ICON
- Ressource RT_GROUP_ICON
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c96e740c23bb61cfdaa6cfbcbf6d0ce7538586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383748"
---
# <a name="icons-menus-and-other-resources"></a>Icônes (menus et autres ressources)

Une *icône* est une image qui se compose d’une image bitmap associée à un masque pour créer des zones transparentes dans l’image. Le terme icône peut faire référence à l’un des éléments suivants :

-   Image d’icône unique. Il s’agit d’une ressource de type **RT \_ icône**.
-   Groupe d’images, à partir duquel le système ou une application peut choisir l’icône la plus appropriée en fonction de la taille et de la profondeur de couleur. Il s’agit d’une ressource de type **\_ \_ icône de groupe RT**.

### <a name="in-this-section"></a>Dans cette section



| Nom                                 | Description                                                 |
|--------------------------------------|-------------------------------------------------------------|
| [À propos des icônes](about-icons.md)       | Décrit les icônes.<br/>                                 |
| [Utilisation des icônes](using-icons.md)       | Explique comment effectuer des tâches liées aux icônes.<br/> |
| [Référence d’icône](icon-reference.md) | Contient la référence de l’API.<br/>                      |



 

### <a name="icon-functions"></a>Icon, fonctions



| Nom                                                               | Description                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)                                       | Copie l’icône spécifiée d’un autre module dans le module en cours. <br/>                                                                                                                                      |
| [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)                                   | Crée une icône qui a la taille, les couleurs et les modèles binaires spécifiés. <br/>                                                                                                                                    |
| [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)           | Crée une icône ou un curseur à partir des bits de ressource qui décrivent l’icône.<br/>                                                                                                                                          |
| [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)       | Crée une icône ou un curseur à partir des bits de ressource qui décrivent l’icône. <br/>                                                                                                                                         |
| [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)                   | Crée une icône ou un curseur à partir d’une structure [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . <br/>                                                                                                                                 |
| [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                 | Détruit une icône et libère la mémoire occupée par l’icône. <br/>                                                                                                                                                  |
| [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)                                       | Dessine une icône ou un curseur dans le contexte de périphérique spécifié.<br/>                                                                                                                                                 |
| [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex)                                   | Dessine une icône ou un curseur dans le contexte de périphérique spécifié, en effectuant les opérations raster spécifiées, et en étirant ou en compressant l’icône ou le curseur comme spécifié. <br/>                                     |
| [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)                             | Crée un doublon d’une icône spécifiée.<br/>                                                                                                                                                                   |
| [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)             | Récupère un handle vers une icône indexée trouvée dans un fichier ou une icône trouvée dans un fichier exécutable associé. <br/>                                                                                                  |
| [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)                                 | Récupère un handle vers une icône à partir du fichier exécutable, de la DLL ou du fichier icône spécifiés.<br/>                                                                                                                        |
| [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)                             | Crée un tableau de handles pour les grandes ou les petites icônes extraites du fichier exécutable, de la DLL ou du fichier d’icône spécifié. <br/>                                                                                      |
| [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)                                 | Récupère des informations sur l’icône ou le curseur spécifié. <br/>                                                                                                                                                 |
| [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)                             | Récupère des informations sur l’icône ou le curseur spécifié. [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa) étend [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) à l’aide de la nouvelle structure [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa) .<br/> |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                                       | Charge la ressource icône spécifiée à partir du fichier exécutable (. exe) associé à une instance d’application.<br/>                                                                                                 |
| [**LookupIconIdFromDirectory**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectory)     | Effectue une recherche dans les données d’icône ou de curseur pour l’icône ou le curseur qui correspond le mieux au périphérique d’affichage actuel.<br/>                                                                                                     |
| [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) | Effectue une recherche dans les données d’icône ou de curseur pour l’icône ou le curseur qui correspond le mieux au périphérique d’affichage actuel. <br/>                                                                                                    |
| [**PrivateExtractIcons**](/windows/desktop/api/Winuser/nf-winuser-privateextracticonsa)                 | Crée un tableau de handles pour les icônes extraites d’un fichier spécifié.<br/>                                                                                                                             |



 

### <a name="icon-structures"></a>Structures d’icône



| Nom                               | Description                                                                                                                                                                                                                                     |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)       | Contient des informations sur une icône ou un curseur. <br/>                                                                                                                                                                                     |
| [**ICONINFOEX**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)   | Contient des informations sur une icône ou un curseur. Étend [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo). Utilisé par [**GetIconInfoEx**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa).<br/>                                                                                                |
| [**ICONMETRICS**](/windows/win32/api/winuser/ns-winuser-iconmetricsa) | Contient les métriques dimensionnables associées aux icônes. Cette structure est utilisée avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) lorsque l’action **SPI \_ GETICONMETRICS** ou **SPI \_ SETICONMETRICS** est spécifiée.<br/> |



 

 

