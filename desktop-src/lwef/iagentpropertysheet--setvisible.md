---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87c67b5a240018dd1798704f5f954c0b5a24fe4b2fc889b1e2d79c892494652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961459"
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


 

 




