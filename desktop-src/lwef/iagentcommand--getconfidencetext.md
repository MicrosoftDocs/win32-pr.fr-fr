---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987dca39016a20d185fbd4b8fd2b554c8bec02f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314658"
---
# <a name="iagentcommandgetconfidencetext"></a><span data-ttu-id="f1ddf-103">IAgentCommand::GetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="f1ddf-103">IAgentCommand::GetConfidenceText</span></span>

<span data-ttu-id="f1ddf-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1ddf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

<span data-ttu-id="f1ddf-105">Récupère le texte info-bulle d’écoute précédemment défini pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f1ddf-105">Retrieves the Listening Tip text previously set for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="f1ddf-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f1ddf-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f1ddf-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span><span class="sxs-lookup"><span data-stu-id="f1ddf-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="f1ddf-108">Adresse d’un BSTR qui reçoit la valeur du texte de l’info-bulle d’écoute pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f1ddf-108">The address of a BSTR that receives the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f1ddf-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1ddf-109">See Also</span></span>

<span data-ttu-id="f1ddf-110">[**IAgentCommand :: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand :: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand :: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="f1ddf-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 