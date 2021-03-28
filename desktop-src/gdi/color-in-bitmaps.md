---
description: Le système gère les couleurs dans les bitmaps différemment des couleurs des stylets, des pinceaux et du texte.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Couleur dans les bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114702"
---
# <a name="color-in-bitmaps"></a>Couleur dans les bitmaps

Le système gère les couleurs dans les bitmaps différemment des couleurs des stylets, des pinceaux et du texte. Les bitmaps compatibles, créées à l’aide de la fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , sont spécifiques aux appareils et conservent les informations de couleur dans un format dépendant du périphérique. Aucune valeur de couleur n’est utilisée, et les couleurs ne sont pas soumises aux approximations et au tramage.

Les bitmaps indépendantes du périphérique (DIB) conservent les informations de couleur en tant que valeurs de couleur ou index de palette de couleurs. Si des valeurs de couleur sont utilisées, les couleurs sont sujettes à approximation, mais pas à l’interpolation. Les index de palette de couleurs ne peuvent être utilisés qu’avec les appareils qui prennent en charge les palettes de couleurs. Bien que le système n’effectue pas de couleurs approximatives ou de trames identifiées par des index, la couleur résultante peut être différente de celle prévue, car les index produisent des résultats valides uniquement dans le contexte de la palette de couleurs actuelle au moment de la création de l’image bitmap. Si la palette change, effectuez les couleurs dans le bitmap. Pour plus d’informations sur les index de palette, consultez [palette par défaut](default-palette.md) et [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).

En plus de faire référence à la palette logique, une application peut également faire référence à une valeur dans une table de couleurs DIB. Pour sélectionner une couleur dans une table de couleurs DIB, appelez [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex). Notez que cela n’est possible que pour un contexte de périphérique pour lequel un DIB est sélectionné.

 

 



