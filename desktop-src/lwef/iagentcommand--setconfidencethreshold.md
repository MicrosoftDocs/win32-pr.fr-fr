---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 244f181fb4d9e706271440797e1261fd381897e00a5a216d681e0f3984d24a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976299"
---
# <a name="iagentcommandsetconfidencethreshold"></a>IAgentCommand::SetConfidenceThreshold

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Définit la valeur de la propriété [**confidence**](confidence-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*
</dt> <dd>

Valeur de la propriété [**confidence**](confidence-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si la valeur de confiance renvoyée par la meilleure correspondance retournée dans l’événement de [**commande**](/windows/desktop/lwef/the-command-object) ne dépasse pas la valeur définie pour la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , le texte fourni dans [**SetConfidenceText**](iagentcommand--setconfidencetext.md) est affiché dans le Conseil d’écoute.

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand :: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 