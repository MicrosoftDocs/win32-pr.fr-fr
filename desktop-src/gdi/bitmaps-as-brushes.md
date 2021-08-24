---
description: Un certain nombre de fonctions utilisent le pinceau actuellement sélectionné dans un contexte de périphérique pour effectuer des opérations de bitmap.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmaps en tant que pinceaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8e218180ab646de1c9c8ff622be1bcc268df73f6f4bb0b6df82482c9a2c851
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944249"
---
# <a name="bitmaps-as-brushes"></a>Bitmaps en tant que pinceaux

Un certain nombre de fonctions utilisent le pinceau actuellement sélectionné dans un contexte de périphérique pour effectuer des opérations de bitmap. Par exemple, la fonction [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) réplique le pinceau dans une zone rectangulaire dans une fenêtre, et la fonction [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) réplique le pinceau à l’intérieur d’une zone dans une fenêtre délimitée par la couleur spécifiée (contrairement à **PatBlt**, **FloodFill** remplit les formes non rectangulaires).

La fonction [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) réplique le pinceau dans une région délimitée par une couleur spécifiée. Toutefois, contrairement à la fonction [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , **FloodFill** ne combine pas les données de couleur du pinceau avec les données de couleur pour les pixels de l’affichage ; Elle définit simplement la couleur de tous les pixels de la zone fermée de l’affichage sur la couleur du pinceau actuellement sélectionné dans le contexte de périphérique.

 

 



