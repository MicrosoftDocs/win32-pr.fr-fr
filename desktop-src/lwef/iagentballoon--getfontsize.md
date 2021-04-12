---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197415"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon::GetFontSize

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Récupère la valeur de la taille de la police affichée dans une bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Adresse d’une valeur qui reçoit la taille de la police.

</dd> </dl>

La taille de police par défaut utilisée dans une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier avec [**IAgentBalloon :: SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). Toutefois, l’utilisateur peut remplacer les paramètres de taille de police pour tous les caractères à l’aide de la feuille de propriétés Microsoft Agent.

 

 




