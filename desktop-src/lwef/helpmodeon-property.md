---
title: Propriété HelpModeOn
description: Propriété HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673482"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="f6f19-103">Propriété HelpModeOn</span><span class="sxs-lookup"><span data-stu-id="f6f19-103">HelpModeOn Property</span></span>

<span data-ttu-id="f6f19-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6f19-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f6f19-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f6f19-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f6f19-106">Retourne ou définit une valeur indiquant si le mode d’aide contextuelle est activé pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="f6f19-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="f6f19-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f6f19-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f6f19-108">\*agent. ***Caractères («*** CharacterID \* \* * »). HelpModeOn* \*  \[  =  *booléen*\]</span><span class="sxs-lookup"><span data-stu-id="f6f19-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="f6f19-109">Partie</span><span class="sxs-lookup"><span data-stu-id="f6f19-109">Part</span></span>      | <span data-ttu-id="f6f19-110">Description</span><span class="sxs-lookup"><span data-stu-id="f6f19-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f19-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f6f19-111">*boolean*</span></span> | <span data-ttu-id="f6f19-112">Expression booléenne spécifiant si le mode d’aide contextuelle est activé.</span><span class="sxs-lookup"><span data-stu-id="f6f19-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="f6f19-113">**True** Le mode d’aide est activé.</span><span class="sxs-lookup"><span data-stu-id="f6f19-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="f6f19-114">Le mode d’aide **false** (par défaut) est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f6f19-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6f19-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f6f19-115">Remarks</span></span>

<span data-ttu-id="f6f19-116">Lorsque vous affectez la valeur **true** à cette propriété, le pointeur de la souris se transforme en image d’aide contextuelle lorsqu’il est déplacé sur le caractère ou sur le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="f6f19-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="f6f19-117">Quand l’utilisateur clique ou fait glisser le caractère ou clique sur un élément dans le menu contextuel du caractère, le serveur déclenche l’événement [**HelpComplete**](helpcomplete-event.md) et quitte le mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="f6f19-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="f6f19-118">Dans le mode d’aide, le serveur n’envoie pas les événements [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)et [**Command**](command-event.md) , sauf si vous affectez la valeur **true** à la propriété [**AutoPopupMenu**](autopopupmenu-property.md) .</span><span class="sxs-lookup"><span data-stu-id="f6f19-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="f6f19-119">Dans ce cas, le serveur enverra l’événement **Click** (ne quitte pas le mode d’aide), mais uniquement pour le bouton droit de la souris pour vous permettre d’afficher le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="f6f19-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="f6f19-120">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="f6f19-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6f19-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6f19-121">See Also</span></span>

[<span data-ttu-id="f6f19-122">**Événement HelpComplete**</span><span class="sxs-lookup"><span data-stu-id="f6f19-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





