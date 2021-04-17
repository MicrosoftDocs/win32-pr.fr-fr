---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380013"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet::GetPage

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Récupère la page active de la feuille de propriétés de l’agent Microsoft.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Adresse d’une variable qui reçoit la page actuelle de la feuille de propriétés (dernière page affichée si la fenêtre n’est pas ouverte). Le paramètre peut avoir l’une des valeurs suivantes :



|                 |                        |
|-----------------|------------------------|
| **Vocale**    | Page d’entrée vocale. |
| **Sortie**    | Page de sortie.       |
| **Intellectuelle** | Page de copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet :: SetPage**](iagentpropertysheet--setpage.md)


 

 




