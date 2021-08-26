---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5535896cc3c40ae3cb04c3078621cc91df4869649cbe72cb106c3d99ec0299ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062019"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Indique si la police utilisée dans une bulle de mot est en italique.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*
</dt> <dd>

Adresse d’une valeur qui reçoit la valeur **true** si la police est en italique et **false** si elle n’est pas en italique.

</dd> </dl>

Le style de police utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent. Elle ne peut pas être modifiée par une application. Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères par le biais de la feuille de propriétés de l’agent Microsoft.

 

 




