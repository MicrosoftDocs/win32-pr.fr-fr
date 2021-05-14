---
description: Événement ShellFolderView. SelectionChanged-se produit lorsque l’état de sélection de tous les éléments de la vue a changé.
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
ms.openlocfilehash: f029ffb217249909e966b592280abf38b2ba2edd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842570"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="6f121-103">Événement ShellFolderView. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="6f121-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="6f121-104">Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.</span><span class="sxs-lookup"><span data-stu-id="6f121-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f121-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f121-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="6f121-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f121-106">Parameters</span></span>

<span data-ttu-id="6f121-107">Ce gestionnaire d’événements n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6f121-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f121-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f121-108">Requirements</span></span>



| <span data-ttu-id="6f121-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f121-109">Requirement</span></span> | <span data-ttu-id="6f121-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f121-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f121-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f121-111">Minimum supported client</span></span><br/> | <span data-ttu-id="6f121-112">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f121-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f121-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f121-113">Minimum supported server</span></span><br/> | <span data-ttu-id="6f121-114">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f121-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6f121-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f121-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f121-116"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f121-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6f121-117">MIDL</span><span class="sxs-lookup"><span data-stu-id="6f121-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f121-118"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f121-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6f121-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6f121-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f121-120"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6f121-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




