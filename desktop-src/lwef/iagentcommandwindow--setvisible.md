---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029406"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow :: SetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Définissez la propriété [**visible**](visible-property.md) pour la fenêtre commandes vocales.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Paramètre de propriété [**visible**](visible-property.md) . La valeur **true** affiche la fenêtre commandes vocales. **False** le masque.

</dd> </dl>

L’utilisateur peut remplacer cette propriété.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandWindow::GetVisible**](iagentcommandwindow--getvisible.md)


 

 




