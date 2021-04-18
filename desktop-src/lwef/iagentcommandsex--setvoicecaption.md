---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509250"
---
# <a name="iagentcommandsexsetvoicecaption"></a><span data-ttu-id="c85e3-103">IAgentCommandsEx::SetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="c85e3-103">IAgentCommandsEx::SetVoiceCaption</span></span>

<span data-ttu-id="c85e3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c85e3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="c85e3-105">Définit le texte [**VoiceCaption**](voicecaption-property.md) affiché pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="c85e3-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="c85e3-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c85e3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c85e3-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="c85e3-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="c85e3-108">BSTR qui spécifie le texte de la propriété [**VoiceCaption**](voicecaption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c85e3-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="c85e3-109">Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c85e3-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="c85e3-110">Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible.</span><span class="sxs-lookup"><span data-stu-id="c85e3-110">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="c85e3-111">Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="c85e3-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="c85e3-112">Lorsque ni la propriété **VoiceCaption** ni **Caption** n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="c85e3-112">When neither the **VoiceCaption** or **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

## <a name="see-also"></a><span data-ttu-id="c85e3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c85e3-113">See Also</span></span>

[<span data-ttu-id="c85e3-114">**IAgentCommandsEx::GetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="c85e3-114">**IAgentCommandsEx::GetVoiceCaption**</span></span>](iagentcommandsex--getvoicecaption.md)


 

 