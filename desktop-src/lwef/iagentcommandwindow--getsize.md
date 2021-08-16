---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200853d88f4f4ea70fce0f80d73f343a2a4d46935a2dfca0ebf78021b0b884ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961579"
---
# <a name="iagentcommandwindowgetsize"></a>IAgentCommandWindow :: est à obtenir

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Récupère la taille actuelle de la fenêtre commandes vocales.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse d’une variable qui reçoit la largeur de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse d’une variable qui reçoit la hauteur de la fenêtre commandes vocales, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommandWindow :: GetPosition**](iagentcommandwindow--getposition.md)


 

 




