---
title: Utilisation des fonctions GDI avec WCS
description: Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Système de couleurs (WCS), GDI (Graphics Device Interface)
- WCS (Windows Color System), GDI (graphics device interface)
- gestion des couleurs des images, GDI (Graphics Device Interface)
- gestion des couleurs, GDI (Graphics Device Interface)
- couleurs, GDI (Graphics Device Interface)
- interface GDI (Graphics Device Interface)
- GDI (Graphics Device Interface)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a104378ae46e6b9519d6f795d280d45c28c8fa3fdc7d1e34aae609bcdbd195d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444676"
---
# <a name="using-gdi-functions-with-wcs"></a>Utilisation des fonctions GDI avec WCS

Il existe différentes fonctions dans l’interface GDI (Graphics Device Interface) qui utilisent ou opèrent sur les données de couleur. Certains sont activés pour une utilisation avec WCS et d’autres non. Les fonctions GDI suivantes s’appliquent à ICM :

-   [Fonctions de contexte de périphérique avec WCS](#device-context-functions-with-wcs)
-   [Fonctions de stylet et de pinceau avec WCS](#pen-and-brush-functions-with-wcs)
-   [Fonctions de sortie de texte avec WCS](#text-output-functions-with-wcs)
-   [Fonctions bitmap avec WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Fonctions de contexte de périphérique avec WCS



|    Fonction                |   Description                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | si le contexte de périphérique (DC) qui est passé à cette fonction par le biais de son paramètre hdc est activé pour ICM, le DC créé par la fonction est également ICM. Les espaces de couleurs source et de destination sont spécifiés dans le DC. |
| CreateDC           | ICM peut être activée en définissant le membre dmICMMethod de la structure DEVMODE vers laquelle pointe le paramètre pInitData sur la valeur appropriée. Pour plus d’informations, consultez la documentation dans le kit de développement Platform SDK sur la structure DEVMODE.  |
| ResetDC            | Le profil de couleurs du contexte de périphérique spécifié par le paramètre HDC sera réinitialisé en fonction des informations contenues dans la structure DEVMODE spécifiée par le paramètre lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Fonctions de stylet et de pinceau avec WCS



|    Fonction                |   Description                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Fonctions de pinceau | Aucune gestion des couleurs n’est effectuée lors de la création du pinceau. toutefois, la gestion des couleurs est effectuée lorsque le pinceau est sélectionné dans un DC ICM. |
| CreatePen       | Aucune gestion des couleurs n’est effectuée lors de la création du stylet. toutefois, la gestion des couleurs est effectuée lorsque le pinceau est sélectionné dans un DC ICM.   |
| ExtCreatePen    | Aucune gestion des couleurs n’est effectuée lors de la création du stylet. toutefois, la gestion des couleurs est effectuée lorsque le pinceau est sélectionné dans un DC ICM.   |
| SelectObject    | Si l’objet sélectionné est un pinceau ou un stylet, la gestion des couleurs est effectuée.                                                              |
| SetDCBrushColor | La gestion des couleurs est effectuée si WCS est activé.                                                                                              |
| SetDCPenColor   | La gestion des couleurs est effectuée si WCS est activé.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Fonctions de sortie de texte avec WCS



|    Fonction                |   Description                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | La gestion des couleurs est effectuée si WCS est activé. |
| SetTextColor | La gestion des couleurs est effectuée si WCS est activé. |



 

## <a name="bitmap-functions-with-wcs"></a>Fonctions bitmap avec WCS



|    Fonction                |   Description                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBlt            | Aucune gestion des couleurs n’est effectuée quand BLITS se produit.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | Le paramètre fuUsage spécifie que le membre bmiColors de la structure BITMAPINFO, pointé par le paramètre lpbmi ne contient pas d’informations sur les couleurs. Si ce n’est pas le cas, aucune gestion des couleurs n’est effectuée pour cette bitmap. La bitmap doit utiliser la version 4 ou la version 5 de la structure BITMAPINFO, pour que la gestion des couleurs soit activée. Le contenu de la bitmap résultante ne correspond pas à la couleur après la création de l’image bitmap. |
| CreateDIBSection  | Si la structure BITMAPINFO, transmise via le paramètre pbmi n’est pas la version 4 ou la version 5, aucune gestion des couleurs n’est effectuée. S’il s’agit de la version 4 ou 5, la gestion des couleurs est activée et l’espace de couleurs spécifié est associé à l’image bitmap.                                                                                                                                                                                                   |
| MaskBlt           | Aucune gestion des couleurs n’est effectuée quand BLITS se produit.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Si l’objet est une bitmap créée avec CreateDIBSection, la gestion des couleurs est effectuée. L’espace colorimétrique de la bitmap est utilisé comme espace colorimétrique de destination.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | La gestion des couleurs est effectuée. Si la structure BITMAPINFO, spécifiée n’est pas la version 4 ou la version 5, le profil de couleurs du contrôleur de domaine actuel est utilisé en tant que profil d’espace de couleurs source. Si ce n’est pas le cas, l’espace sRVB est utilisé. Si la structure BITMAPINFO, spécifiée est la version 4 ou la version 5, le profil d’espace colorimétrique spécifié dans l’en-tête bitmap est utilisé comme profil d’espace colorimétrique source.                                         |
| SetDIBitsToDevice | La gestion des couleurs est effectuée. Si la structure BITMAPINFO, spécifiée n’est pas la version 4 ou la version 5, le profil de couleurs du contexte de périphérique actuel est utilisé en tant que profil d’espace de couleurs source. Si ce n’est pas le cas, l’espace de couleurs sRVB est utilisé. Si la structure BITMAPINFO, spécifiée est la version 4 ou la version 5, le profil d’espace colorimétrique associé à la bitmap est utilisé comme espace de couleur source.                                    |
| SetDIBColorTable  | Aucune gestion des couleurs n’est effectuée.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Aucune gestion des couleurs n’est effectuée quand BLITS se produit.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | La gestion des couleurs est effectuée. Si la structure BITMAPINFO, spécifiée n’est pas la version 4 ou la version 5, le profil de couleurs du contrôleur de domaine actuel est utilisé en tant que profil d’espace de couleurs source. Si ce n’est pas le cas, l’espace sRVB est utilisé. Si la structure BITMAPINFO, spécifiée est la version 4 ou la version 5, le profil d’espace colorimétrique spécifié dans l’en-tête bitmap est utilisé comme profil d’espace colorimétrique source.                                         |



 

 

 




