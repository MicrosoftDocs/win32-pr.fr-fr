---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031074"
---
# <a name="iagentcommandexsetvoicecaption"></a><span data-ttu-id="75d73-103">IAgentCommandEx::SetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="75d73-103">IAgentCommandEx::SetVoiceCaption</span></span>

<span data-ttu-id="75d73-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75d73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="75d73-105">Définit le texte [**VoiceCaption**](voicecaption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="75d73-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="75d73-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="75d73-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="75d73-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="75d73-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="75d73-108">BSTR qui spécifie le texte de la propriété [**VoiceCaption**](voicecaption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="75d73-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="75d73-109">Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="75d73-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="75d73-110">Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est entrée active.</span><span class="sxs-lookup"><span data-stu-id="75d73-110">This text will appear in the Voice Commands Window when your client application is input active.</span></span> <span data-ttu-id="75d73-111">Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="75d73-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="75d73-112">Lorsque ni la propriété **VoiceCaption** ni la propriété n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="75d73-112">When neither the **VoiceCaption** or property is set, the command does not appear in the Voice Commands Window.</span></span>

[<span data-ttu-id="75d73-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="75d73-113">**Caption**</span></span>](caption-property.md)

## <a name="see-also"></a><span data-ttu-id="75d73-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d73-114">See Also</span></span>

<span data-ttu-id="75d73-115">[**IAgentCommand :: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx :: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx :: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="75d73-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 