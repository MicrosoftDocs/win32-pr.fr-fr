---
title: IAgentCommand GetVisible
description: IAgentCommand GetVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381934"
---
# <a name="iagentcommandgetvisible"></a><span data-ttu-id="414ee-103">IAgentCommand::GetVisible</span><span class="sxs-lookup"><span data-stu-id="414ee-103">IAgentCommand::GetVisible</span></span>

<span data-ttu-id="414ee-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="414ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

<span data-ttu-id="414ee-105">Récupère la valeur de la propriété [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="414ee-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="414ee-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="414ee-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="414ee-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="414ee-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="414ee-108">Adresse d’une variable qui reçoit la propriété [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="414ee-108">The address of a variable that receives the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="414ee-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414ee-109">See Also</span></span>

<span data-ttu-id="414ee-110">[**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="414ee-110">[**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 