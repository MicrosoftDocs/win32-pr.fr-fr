---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511425df848749791d2803a484e00da8e838cfa191eade05c578fdad4b3ca6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105197"
---
# <a name="iagentcommandsexsetfontname"></a>IAgentCommandsEx::SetFontName

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

Définit la police affichée dans le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

BSTR qui définit la police affichée dans le menu contextuel du caractère.

</dd> </dl>

Cette propriété détermine la police utilisée pour afficher le texte dans le menu contextuel du caractère. La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère, ou si ce n’est pas le cas, le paramètre ID de langue par défaut de l’utilisateur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx :: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx :: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx :: SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




