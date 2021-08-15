---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92319178f2fbceb7b2e0cad9bdb35b740ebeaf108f864edb84b4413353e85e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477201"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx::SetFontSize

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Définit la taille de la police affichée dans le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Taille de la police.

</dd> </dl>

Cette propriété détermine la taille en points de la police utilisée pour afficher le texte dans le menu contextuel du caractère quand votre application cliente est active en entrée. La valeur par défaut du paramètre font est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère, ou si ce n’est pas le cas, il s’agit du paramètre de langue par défaut de l’utilisateur. S’il n’est pas en entrée-actif, le texte de la [**légende**](caption-property.md) de [**commande**](/windows/desktop/lwef/the-command-object) de votre application cliente apparaît dans la taille en points spécifiée pour le client d’entrée-actif.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx :: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx :: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx :: SetFontName**](iagentcommandsex--setfontname.md)


 

 