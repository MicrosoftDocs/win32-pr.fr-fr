---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310214"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet::GetVisible

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Détermine si la feuille de propriétés Microsoft Agent est visible ou masquée.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** si la feuille de propriétés est visible et **false** si elle est masquée.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet :: SetVisible**](iagentpropertysheet--setvisible.md)


 

 




