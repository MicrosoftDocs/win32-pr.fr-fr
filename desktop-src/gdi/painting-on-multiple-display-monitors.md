---
description: Le système gère automatiquement le dessin dans un contexte de périphérique (DC) qui couvre plusieurs moniteurs, même lorsque les moniteurs ont des profondeurs de couleurs différentes.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Peinture sur plusieurs moniteurs d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754341"
---
# <a name="painting-on-multiple-display-monitors"></a>Peinture sur plusieurs moniteurs d’affichage

Le système gère automatiquement le dessin dans un contexte de périphérique (DC) qui couvre plusieurs moniteurs, même lorsque les moniteurs ont des profondeurs de couleurs différentes. En général, cela produit de bons résultats, mais il peut ne pas être optimal. Par exemple, une fenêtre sur deux moniteurs de palettes de couleurs très différentes peut avoir un rendu de couleur médiocre. En outre, les analyses avec la même profondeur de couleur peuvent avoir un exemple de formatsfor de couleur différent, les couleurs peuvent être encodées avec différents nombres de bits ou se trouver à des emplacements différents dans la valeur de couleur d’un pixel.

Pour obtenir les meilleurs résultats pour chaque moniteur d’un contrôleur de domaine qui s’étend sur plusieurs affichages, appelez [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) pour énumérer les moniteurs qui croisent votre contrôleur de domaine et peignez la zone d’intersection dans chacune d’elles séparément en fonction des attributs d’affichage de cette analyse. Consultez l’exemple relatif à la [peinture sur un contrôleur de périphérique qui s’étend sur plusieurs affichages](painting-on-a-dc-that-spans-multiple-displays.md).

Si vous effectuez tout le dessin dans votre code **de \_ peinture WM** et si votre code de **\_ peinture WM** gère tous les différents modes vidéo, vous devez être en mesure de placer votre code de **\_ peinture WM** dans le **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) avec quelques modifications uniquement.

 

 



