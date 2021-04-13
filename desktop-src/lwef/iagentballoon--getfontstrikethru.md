---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380350"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBalloon::GetFontStrikethru

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Indique si la police utilisée dans une bulle de mot a le style barré défini.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*
</dt> <dd>

Adresse d’une valeur qui reçoit la valeur **true** si le style de police barré est défini et **false** dans le cas contraire.

</dd> </dl>

Le style de police utilisé dans une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent. Elle ne peut pas être modifiée par une application. Toutefois, l’utilisateur peut remplacer les paramètres de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.

 

 




