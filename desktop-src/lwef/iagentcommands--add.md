---
title: IAgentCommands ajouter
description: IAgentCommands ajouter
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101481"
---
# <a name="iagentcommandsadd"></a><span data-ttu-id="2e536-103">IAgentCommands :: Add</span><span class="sxs-lookup"><span data-stu-id="2e536-103">IAgentCommands::Add</span></span>

<span data-ttu-id="2e536-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e536-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
);
```

<span data-ttu-id="2e536-105">Ajoute une [**commande**](/windows/desktop/lwef/the-command-object) à une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2e536-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="2e536-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2e536-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2e536-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="2e536-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="2e536-108">BSTR qui spécifie la valeur du texte de [**légende**](caption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2e536-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="2e536-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="2e536-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="2e536-110">BSTR qui spécifie la valeur du paramètre de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2e536-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="2e536-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="2e536-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="2e536-112">Expression booléenne qui spécifie le paramètre [**activé**](enabled-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2e536-112">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="2e536-113">Si le paramètre a la **valeur true**, la **commande** est activée et peut être sélectionnée. Si la **valeur est false**, la **commande** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2e536-113">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="2e536-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="2e536-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2e536-115">Expression booléenne qui spécifie le paramètre [**visible**](visible-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2e536-115">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="2e536-116">Si le paramètre a la **valeur true**, la **commande** est visible dans le menu contextuel du caractère (si la propriété [**Caption**](caption-property.md) est également définie).</span><span class="sxs-lookup"><span data-stu-id="2e536-116">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="2e536-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="2e536-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="2e536-118">Adresse d’une variable qui reçoit l’ID de la [**commande**](/windows/desktop/lwef/the-command-object)ajoutée.</span><span class="sxs-lookup"><span data-stu-id="2e536-118">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2e536-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e536-119">See Also</span></span>

<span data-ttu-id="2e536-120">[**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md), [**IAgentCommands :: Remove**](iagentcommands--remove.md), [**IAgentCommands :: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="2e536-120">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 