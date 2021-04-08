---
title: Fonctions de format de pixel
description: Les fonctions Windows suivantes gèrent les formats de pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Fonctions WGL, format de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840769"
---
# <a name="pixel-format-functions"></a>Fonctions de format de pixel

Les fonctions Windows suivantes gèrent les formats de pixel.



| Fonction Windows                                               | Description                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Obtient le format de pixel du contexte de périphérique qui correspond le plus à un format de pixel spécifié.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Définit le format de pixel actuel d’un contexte de périphérique au format de pixel spécifié par un index de format de pixel.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Obtient l’index de format de pixel du format de pixel actuel d’un contexte de périphérique.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Étant donné un contexte de périphérique et un index de format de pixel, remplit une structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) avec les propriétés du format de pixel. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Récupère les informations de format de pixel pour un métafichier amélioré.                                                                                                          |



 

La fonction [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) retourne un index de format de pixel de base 1 qui identifie la meilleure correspondance à partir des formats de pixel pris en charge du contexte de périphérique.

La fonction [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifie le format souhaité à l’aide d’un index de format de pixel de base 1. En général, vous appelez **ChoosePixelFormat** pour rechercher un format de pixel le mieux adapté, puis vous appelez **SetPixelFormat** avec le résultat de **ChoosePixelFormat**.

Si vous appelez **SetPixelFormat** pour un contexte de périphérique qui référence une fenêtre, **SetPixelFormat** modifie également le format de pixel de la fenêtre. La définition du format de pixel d’une fenêtre plusieurs fois peut entraîner des complications significatives pour le gestionnaire de fenêtres et pour les applications multithread, ce qui n’est donc pas autorisé. Vous ne pouvez définir le format de pixel d’une fenêtre qu’une seule fois ; Après cela, le format de pixel de la fenêtre ne peut pas être modifié.

La fonction [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) retourne un index de format de pixel de base un.

La fonction [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) prend les valeurs suivantes comme paramètres :

-   Handle vers un contexte de périphérique (Device Context)
-   Un index de format de pixel
-   Pointeur vers une structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

La fonction [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) retourne avec les membres de **PIXELFORMATDESCRIPTOR** définis de manière appropriée.

La fonction **GetEnhMetaFilePixelFormat** retourne la taille du format de pixel d’un métafichier et récupère les informations de format de pixel du métafichier.

 

 




