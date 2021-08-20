---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6eabb7278e40030209ac85f55c3a7d5c00edda5c666493e053dfcbfae2ecd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692460"
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



|                 | Description            |
|-----------------|------------------------|
| **Vocale**    | Page d’entrée vocale. |
| **Sortie**    | Page de sortie.       |
| **Intellectuelle** | Page de copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet :: SetPage**](iagentpropertysheet--setpage.md)


 

 




