---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031114"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="92c2d-103">IAgentCommand::SetEnabled</span><span class="sxs-lookup"><span data-stu-id="92c2d-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="92c2d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="92c2d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="92c2d-105">Définit la propriété [**Enabled**](enabled-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="92c2d-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="92c2d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="92c2d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="92c2d-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="92c2d-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="92c2d-108">Valeur booléenne qui définit la valeur du paramètre [**activé**](enabled-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="92c2d-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="92c2d-109">**True** active la **commande**; **False** le désactive.</span><span class="sxs-lookup"><span data-stu-id="92c2d-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="92c2d-110">Impossible de sélectionner une **commande** désactivée.</span><span class="sxs-lookup"><span data-stu-id="92c2d-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="92c2d-111">La propriété [**Enabled**](enabled-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object) doit être définie sur **true** pour pouvoir être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="92c2d-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="92c2d-112">Elle doit également avoir la propriété [**Caption**](caption-property.md) définie et sa propriété [**visible**](visible-property.md) définie sur **true** pour s’afficher dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="92c2d-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="92c2d-113">Pour que la **commande** s’affiche dans la **fenêtre commandes vocales**, vous devez définir sa propriété [**Voice**](voice-property.md).</span><span class="sxs-lookup"><span data-stu-id="92c2d-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="92c2d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92c2d-114">See Also</span></span>

<span data-ttu-id="92c2d-115">[**IAgentCommand :: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="92c2d-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 