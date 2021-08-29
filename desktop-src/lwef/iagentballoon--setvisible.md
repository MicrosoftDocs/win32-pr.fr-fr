---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c821d4e3686a9e454798cb80a85f3047f8cbdbaf57c075dae1361db6606d4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478593"
---
# <a name="iagentballoonsetvisible"></a>IAgentBalloon :: SetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

Définit la propriété [**visible**](visible-property.md) pour le mot-bulle.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Paramètre de propriété visible. La valeur **true** affiche le mot-bulle. la valeur **false** le masque.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetVisible**](iagentballoon--getvisible.md)


 

 




