---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101616"
---
# <a name="iagentcommandsetconfidencethreshold"></a><span data-ttu-id="f31c1-103">IAgentCommand::SetConfidenceThreshold</span><span class="sxs-lookup"><span data-stu-id="f31c1-103">IAgentCommand::SetConfidenceThreshold</span></span>

<span data-ttu-id="f31c1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f31c1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

<span data-ttu-id="f31c1-105">Définit la valeur de la propriété [**confidence**](confidence-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f31c1-105">Sets the value of the [**Confidence**](confidence-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="f31c1-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f31c1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f31c1-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span><span class="sxs-lookup"><span data-stu-id="f31c1-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="f31c1-108">Valeur de la propriété [**confidence**](confidence-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f31c1-108">The value for the [**Confidence**](confidence-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="f31c1-109">Si la valeur de confiance renvoyée par la meilleure correspondance retournée dans l’événement de [**commande**](/windows/desktop/lwef/the-command-object) ne dépasse pas la valeur définie pour la propriété [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , le texte fourni dans [**SetConfidenceText**](iagentcommand--setconfidencetext.md) est affiché dans le Conseil d’écoute.</span><span class="sxs-lookup"><span data-stu-id="f31c1-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="f31c1-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f31c1-110">See Also</span></span>

<span data-ttu-id="f31c1-111">[**IAgentCommand :: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand :: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="f31c1-111">[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 