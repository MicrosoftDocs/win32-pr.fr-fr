---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380352"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon::GetFontName

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Récupère la valeur de la police affichée dans une bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Adresse d’un BSTR qui reçoit le nom de police affiché dans une bulle de mot.

</dd> </dl>

La police par défaut utilisée dans une bulle de mot de caractères est définie dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier avec [**IAgentBalloon :: SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**). L’utilisateur peut remplacer le paramètre de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.

 

 




