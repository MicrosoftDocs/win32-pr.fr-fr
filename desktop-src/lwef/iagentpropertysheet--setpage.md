---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120744"
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



|                 | Description            |
|-----------------|------------------------|
| **Vocale**    | Page d’entrée vocale. |
| **Sortie**    | Page de sortie.       |
| **Intellectuelle** | Page de copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




