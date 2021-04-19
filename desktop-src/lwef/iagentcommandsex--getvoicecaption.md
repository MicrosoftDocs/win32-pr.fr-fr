---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a757e1c841afd62b9b6ae13f1ef34178f133ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106543047"
---
# <a name="iagentcommandsexgetvoicecaption"></a><span data-ttu-id="8a605-103">IAgentCommandsEx::GetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="8a605-103">IAgentCommandsEx::GetVoiceCaption</span></span>

<span data-ttu-id="8a605-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8a605-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

<span data-ttu-id="8a605-105">Récupère le [**VoiceCaption**](voicecaption-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="8a605-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="8a605-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8a605-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8a605-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="8a605-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="8a605-108">Adresse d’un BSTR qui reçoit la valeur du texte de [**légende**](caption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="8a605-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="8a605-109">Le texte retourné est celui défini pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) et apparaît dans la fenêtre commandes vocales lorsque votre application cliente est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="8a605-109">The text returned is that set for your [**Command**](/windows/desktop/lwef/the-command-object) object and appears in the Voice Commands window when your client application is input-active.</span></span>

<span data-ttu-id="8a605-110">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="8a605-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a605-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a605-111">See Also</span></span>

[<span data-ttu-id="8a605-112">**IAgentCommandsEx::SetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="8a605-112">**IAgentCommandsEx::SetVoiceCaption**</span></span>](iagentcommandsex--setvoicecaption.md)


 

 