---
title: IAgentBalloon SetFontName
description: IAgentBalloon SetFontName
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029795"
---
# <a name="iagentballoonsetfontname"></a>IAgentBalloon::SetFontName

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Définit la police affichée dans la bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

BSTR qui définit la police affichée dans la bulle de mot.

</dd> </dl>

La police par défaut utilisée dans la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier avec **IAgentBalloon :: SetFontName**. Toutefois, l’utilisateur peut remplacer le paramètre de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetVisible**](iagentballoon--getvisible.md)


 

 




