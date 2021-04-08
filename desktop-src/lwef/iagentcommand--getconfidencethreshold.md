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
# <a name="iagentcommandgetconfidencethreshold"></a><span data-ttu-id="cf67c-103">IAgentCommand::GetConfidenceThreshold</span><span class="sxs-lookup"><span data-stu-id="cf67c-103">IAgentCommand::GetConfidenceThreshold</span></span>

<span data-ttu-id="cf67c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf67c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

<span data-ttu-id="cf67c-105">Récupère la valeur de la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="cf67c-105">Retrieves the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="cf67c-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="cf67c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cf67c-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*</span><span class="sxs-lookup"><span data-stu-id="cf67c-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*</span></span>
</dt> <dd>

<span data-ttu-id="cf67c-108">Adresse d’une variable qui reçoit la valeur de la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) pour une commande.</span><span class="sxs-lookup"><span data-stu-id="cf67c-108">The address of a variable that receives the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a Command.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="cf67c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf67c-109">See Also</span></span>

<span data-ttu-id="cf67c-110">[**IAgentCommand :: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand :: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="cf67c-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 