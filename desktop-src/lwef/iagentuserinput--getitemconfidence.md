---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309141"
---
# <a name="iagentuserinputgetitemconfidence"></a><span data-ttu-id="d3933-103">IAgentUserInput::GetItemConfidence</span><span class="sxs-lookup"><span data-stu-id="d3933-103">IAgentUserInput::GetItemConfidence</span></span>

<span data-ttu-id="d3933-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d3933-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

<span data-ttu-id="d3933-105">Récupère la valeur de confiance pour une [**commande**](command-event.md) passée à un rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="d3933-105">Retrieves the confidence value for a [**Command**](command-event.md) passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="d3933-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d3933-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d3933-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="d3933-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="d3933-108">L’index d’une alternative de [**commande**](command-event.md) a été passé au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="d3933-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="d3933-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span><span class="sxs-lookup"><span data-stu-id="d3933-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="d3933-110">Adresse d’une variable qui reçoit le score de confiance pour une autre [**commande**](command-event.md) passée au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="d3933-110">Address of a variable that receives the confidence score for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="d3933-111">Si l’entrée vocale n’est pas la source de la commande, par exemple si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur Microsoft Agent renvoie la valeur de confiance de la meilleure correspondance comme 100 et les valeurs de confiance pour toutes les autres alternatives comme zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d3933-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the confidence value of the best match as 100 and the confidence values for all other alternatives as zero (0).</span></span>

## <a name="see-also"></a><span data-ttu-id="d3933-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3933-112">See Also</span></span>

<span data-ttu-id="d3933-113">[**IAgentUserInput :: getItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput :: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput :: GetItemText**](iagentuserinput--getitemtext.md)</span><span class="sxs-lookup"><span data-stu-id="d3933-113">[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)</span></span>


 

 




