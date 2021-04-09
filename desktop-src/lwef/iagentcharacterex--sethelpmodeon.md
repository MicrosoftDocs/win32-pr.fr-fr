---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101497"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="60c39-103">IAgentCharacterEx::SetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="60c39-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="60c39-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60c39-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="60c39-105">Définit le mode d’aide contextuelle pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="60c39-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="60c39-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="60c39-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="60c39-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="60c39-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="60c39-108">Indicateur du mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="60c39-108">Help mode flag.</span></span> <span data-ttu-id="60c39-109">Si ce paramètre a la **valeur true**, Microsoft Agent active le mode d’aide pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="60c39-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="60c39-110">Lorsque vous affectez la valeur **true** à cette propriété, le pointeur de la souris se transforme en image d’aide contextuelle lorsqu’il est déplacé sur le caractère ou sur le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="60c39-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="60c39-111">Quand l’utilisateur clique ou fait glisser le caractère ou clique sur un élément dans le menu contextuel du caractère, le serveur déclenche l’événement [**IAgentNotifySinkEx :: HelpComplete**](iagentnotifysinkex--helpcomplete.md) et quitte le mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="60c39-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="60c39-112">Dans le mode d’aide, le serveur n’envoie pas les événements [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)et [**Command**](command-event.md) , sauf si la propriété [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="60c39-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="60c39-113">Dans ce cas, le serveur enverra l’événement **Click** (ne quitte pas le mode d’aide), mais uniquement pour le bouton droit de la souris afin que vous puissiez afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="60c39-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="60c39-114">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="60c39-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="60c39-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60c39-115">See Also</span></span>

<span data-ttu-id="60c39-116">[**IAgentCharacterEx :: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx :: HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="60c39-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 