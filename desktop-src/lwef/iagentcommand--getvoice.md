---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512496"
---
# <a name="iagentcommandgetvoice"></a><span data-ttu-id="00d1d-103">IAgentCommand::GetVoice</span><span class="sxs-lookup"><span data-stu-id="00d1d-103">IAgentCommand::GetVoice</span></span>

<span data-ttu-id="00d1d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="00d1d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

<span data-ttu-id="00d1d-105">Récupère la valeur de la propriété de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="00d1d-105">Retrieves the value of the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="00d1d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="00d1d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="00d1d-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="00d1d-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="00d1d-108">Adresse d’un BSTR qui reçoit la propriété de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="00d1d-108">The address of a BSTR that receives the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="00d1d-109">Une [**commande**](/windows/desktop/lwef/the-command-object) dont la propriété [**Voice**](voice-property.md) est définie et dont la propriété [**Enabled**](enabled-property.md) a la valeur **true** est accessible en voix.</span><span class="sxs-lookup"><span data-stu-id="00d1d-109">A [**Command**](/windows/desktop/lwef/the-command-object) with its [**Voice**](voice-property.md) property set and its [**Enabled**](enabled-property.md) property set to **True** will be voice-accessible.</span></span> <span data-ttu-id="00d1d-110">Si sa propriété [**Caption**](caption-property.md) est également définie, elle apparaît dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="00d1d-110">If its [**Caption**](caption-property.md) property is also set it appears in the Voice Commands Window.</span></span> <span data-ttu-id="00d1d-111">Si sa propriété [**visible**](visible-property.md) a la valeur **true**, elle apparaît dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="00d1d-111">If its [**Visible**](visible-property.md) property is set to **True**, it appears in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="00d1d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00d1d-112">See Also</span></span>

<span data-ttu-id="00d1d-113">[**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="00d1d-113">[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 