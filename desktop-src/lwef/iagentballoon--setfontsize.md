---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311215"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon::SetFontSize

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Définit la taille de la police affichée dans la bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Taille de la police.

</dd> </dl>

La taille de police par défaut utilisée dans la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier avec **IAgentBalloon :: SetFontSize**. Toutefois, l’utilisateur peut remplacer le paramètre de taille de police pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetFontSize**](iagentballoon--getfontsize.md)


 

 




