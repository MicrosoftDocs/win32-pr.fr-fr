---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673769"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet :: SetPage

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Définit la page active de la feuille de propriétés de l’agent Microsoft.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

BSTR qui définit la page actuelle de la propriété. Le paramètre peut avoir l’une des valeurs suivantes.



|                 |                        |
|-----------------|------------------------|
| **Vocale**    | Page d’entrée vocale. |
| **Sortie**    | Page de sortie.       |
| **Intellectuelle** | Page de copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




