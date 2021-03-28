---
description: Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.
title: Événement ShellFolderView. SelectionChanged (shldisp. h)
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
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: 864cd4c7bb0b414e4237c698412ad10899c8cbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035100"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="1de51-103">Événement ShellFolderView. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="1de51-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="1de51-104">Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1de51-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1de51-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="1de51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1de51-106">Parameters</span></span>

<span data-ttu-id="1de51-107">Ce gestionnaire d’événements n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1de51-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de51-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1de51-108">Requirements</span></span>



| <span data-ttu-id="1de51-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1de51-109">Requirement</span></span> | <span data-ttu-id="1de51-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1de51-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de51-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1de51-111">Minimum supported client</span></span><br/> | <span data-ttu-id="1de51-112">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1de51-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1de51-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1de51-113">Minimum supported server</span></span><br/> | <span data-ttu-id="1de51-114">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1de51-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1de51-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="1de51-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="1de51-116"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1de51-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1de51-117">MIDL</span><span class="sxs-lookup"><span data-stu-id="1de51-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1de51-118"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1de51-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1de51-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1de51-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1de51-120"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1de51-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




