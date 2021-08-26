---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1d5894a04eeb09289e98db42362acbc43d587e5ac680b98276260ba9c323b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961929"
---
# <a name="iagentcommandgetconfidencetext"></a>IAgentCommand::GetConfidenceText

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

Récupère le texte info-bulle d’écoute précédemment défini pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du texte de l’info-bulle d’écoute pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand :: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand :: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 