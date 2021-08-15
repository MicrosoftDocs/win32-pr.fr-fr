---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8889c8c8c52f392a368c38a91510e112adbeeca42c611cdc0adcadad94f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976339"
---
# <a name="iagentcommandsetconfidencetext"></a>IAgentCommand::SetConfidenceText

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

Définit la valeur du texte info-bulle d’écoute pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*
</dt> <dd>

BSTR qui spécifie le texte de la propriété [**ConfidenceText**](confidencetext-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si la valeur de confiance renvoyée par la meilleure correspondance retournée dans l’événement de [**commande**](/windows/desktop/lwef/the-command-object) ne dépasse pas la valeur définie pour la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , le texte fourni dans *BszTipText* est affiché dans le Conseil d’écoute.

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand :: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand :: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 