---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028472"
---
# <a name="iagentuserinputgetitemtext"></a><span data-ttu-id="b22f8-103">IAgentUserInput::GetItemText</span><span class="sxs-lookup"><span data-stu-id="b22f8-103">IAgentUserInput::GetItemText</span></span>

<span data-ttu-id="b22f8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b22f8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

<span data-ttu-id="b22f8-105">Récupère le texte vocal pour une autre [**commande**](command-event.md) passée au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="b22f8-105">Retrieves the voice text for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="b22f8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b22f8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b22f8-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="b22f8-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="b22f8-108">L’index d’une alternative de [**commande**](command-event.md) a été passé au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="b22f8-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="b22f8-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="b22f8-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="b22f8-110">Adresse d’un BSTR qui reçoit la valeur du texte vocal de la [**commande**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="b22f8-110">Address of a BSTR that receives the value of the voice text for the [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="b22f8-111">Si l’entrée vocale n’est pas la source de la commande, par exemple si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur renvoie la **valeur null** pour le texte vocal de la [**commande**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="b22f8-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the server returns **NULL** for the [**Command**](command-event.md)'s voice text.</span></span>

## <a name="see-also"></a><span data-ttu-id="b22f8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b22f8-112">See Also</span></span>

<span data-ttu-id="b22f8-113">[**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput :: getItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput :: GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="b22f8-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




