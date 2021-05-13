---
description: Indique que l’état de sélection d’un ou plusieurs éléments de la vue a changé.
title: Événement ShellFolderViewOC. SelectionChanged (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 53d6fc3eb6f13d136af603a3129ba75a46c3c6a6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841040"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="5a3c4-103">Événement ShellFolderViewOC. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="5a3c4-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="5a3c4-104">Indique que l’état de sélection d’un ou plusieurs éléments de la vue a changé.</span><span class="sxs-lookup"><span data-stu-id="5a3c4-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a3c4-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="5a3c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a3c4-106">Parameters</span></span>

<span data-ttu-id="5a3c4-107">Ce gestionnaire d’événements n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5a3c4-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a3c4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5a3c4-108">Remarks</span></span>

<span data-ttu-id="5a3c4-109">Fournissez le code de gestion des événements pour cet événement, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="5a3c4-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="5a3c4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5a3c4-110">Requirements</span></span>



| <span data-ttu-id="5a3c4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a3c4-111">Requirement</span></span> | <span data-ttu-id="5a3c4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a3c4-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3c4-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a3c4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3c4-114">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a3c4-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a3c4-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a3c4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3c4-116">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a3c4-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5a3c4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a3c4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3c4-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3c4-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5a3c4-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="5a3c4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a3c4-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a3c4-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5a3c4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5a3c4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a3c4-122"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5a3c4-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3c4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a3c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3c4-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="5a3c4-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




