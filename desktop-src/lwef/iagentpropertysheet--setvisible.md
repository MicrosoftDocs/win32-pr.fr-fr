---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511430"
---
# <a name="iagentpropertysheetsetvisible"></a>IAgentPropertySheet :: SetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

Définit la propriété [**visible**](visible-property.md) pour la feuille de propriétés de l’agent Microsoft.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Paramètre de propriété visible. La valeur **true** affiche la feuille de propriétés ; la valeur **false** le masque.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet::GetVisible**](iagentpropertysheet--getvisible.md)


 

 




