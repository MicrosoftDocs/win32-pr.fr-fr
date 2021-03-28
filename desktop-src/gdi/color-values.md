---
description: La couleur est définie sous la forme d’une combinaison de trois couleurs primaires rouge, vert et bleu.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valeurs de couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114694"
---
# <a name="color-values"></a>Valeurs de couleur

La couleur est définie sous la forme d’une combinaison de trois couleurs primaires rouge, vert et bleu. le système identifie une couleur en lui attribuant une valeur de couleur (parfois appelée triplet RVB), qui se compose de valeurs 3 8 bits spécifiant les intensités de ses composants de couleur. Le noir présente l’intensité minimale pour le rouge, le vert et le bleu, donc la valeur de couleur pour le noir est (0, 0, 0). Le blanc a l’intensité maximale pour le rouge, le vert et le bleu, donc sa valeur de couleur est (255, 255, 255).

> [!Note]  
> Si la correspondance des couleurs de l’image est activée, la définition de la couleur et la signification d’une valeur de couleur dépendent du type d’espace de couleurs actuellement défini pour le contexte de périphérique.

 

Le système et les applications utilisent des paramètres et des variables dont le type [COLORREF](colorref.md) permet de transmettre et de stocker des valeurs de couleur. Par exemple, la fonction [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifie la couleur de chaque stylet en affectant une valeur de couleur au membre **lopnColor** dans une structure [**logpen,**](/windows/win32/api/wingdi/ns-wingdi-logpen) . Les applications peuvent extraire les valeurs individuelles des composants rouge, vert et bleu d’une valeur de couleur à l’aide des macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)et [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivement. Les applications peuvent créer une valeur de couleur à partir de valeurs de composants individuels à l’aide de la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) . Lors de la création ou de l’examen d’une palette logique, une application utilise la structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) pour définir les valeurs de couleur et pour examiner les valeurs des composants individuels.

 

 



