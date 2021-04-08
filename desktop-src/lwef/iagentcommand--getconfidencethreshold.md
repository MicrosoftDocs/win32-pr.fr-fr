---
title: IAgentCommand GetConfidenceThreshold
description: IAgentCommand GetConfidenceThreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6557ad4e6831734106ee2c2e8021f923ef8806
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725948"
---
# <a name="iagentcommandgetconfidencethreshold"></a>IAgentCommand::GetConfidenceThreshold

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

Récupère la valeur de la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*
</dt> <dd>

Adresse d’une variable qui reçoit la valeur de la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) pour une commande.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand :: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 