---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc392bd12fccfb01b8aee41a5a06ed50b388ac8223e622d75218c840f706c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962489"
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

 

 




