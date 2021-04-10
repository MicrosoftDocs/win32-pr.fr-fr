---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197284"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="77292-103">IAgentCharacterEx::GetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="77292-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="77292-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77292-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="77292-105">Récupère une valeur indiquant si le mode d’aide contextuelle est activé pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="77292-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="77292-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="77292-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="77292-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="77292-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="77292-108">Adresse d’une variable qui reçoit **true** si le mode d’aide est activé pour le caractère et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="77292-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="77292-109">Lorsque cette propriété est définie sur **true**, le pointeur de la souris se transforme en image d’aide contextuelle lorsqu’il est déplacé sur le caractère ou sur le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="77292-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="77292-110">Quand l’utilisateur clique ou fait glisser le caractère ou clique sur un élément dans le menu contextuel du caractère, le serveur déclenche l’événement [**IAgentNotifySinkEx :: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) et quitte le mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="77292-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="77292-111">En mode d’aide, le serveur n’envoie pas les événements [**IAgentNotifySink :: Click**](iagentnotifysink--click.md), [**IAgentNotifySink ::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink ::D Ragcomplete**](iagentnotifysink--dragcomplete.md)et [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) , sauf si la propriété [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="77292-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="77292-112">Dans ce cas, le serveur enverra l’événement **IAgentNotifySink :: Click** (ne quitte pas le mode d’aide), mais uniquement pour le bouton droit de la souris pour vous permettre d’afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="77292-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="77292-113">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="77292-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="77292-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77292-114">See Also</span></span>

[<span data-ttu-id="77292-115">**IAgentCharacterEx::SetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="77292-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 




