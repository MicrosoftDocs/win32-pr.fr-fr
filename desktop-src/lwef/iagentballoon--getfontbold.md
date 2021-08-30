---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc48eeba39a889c5a7cbee9bc9caeef759571e98b904646c62cd903c444305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962609"
---
# <a name="iagentballoongetfontbold"></a>IAgentBalloon::GetFontBold

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

Indique si la police utilisée dans une bulle de mot est en gras.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*
</dt> <dd>

Adresse d’une valeur qui reçoit la valeur **true** si la police est en gras et **false** si elle n’est pas en gras.

</dd> </dl>

Le style de police utilisé dans une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent. Elle ne peut pas être modifiée par une application. Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.

 

 




