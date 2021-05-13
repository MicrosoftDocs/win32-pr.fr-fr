---
description: Indique que l’objet ShellFolderView a terminé l’énumération du contenu du dossier.
title: Événement ShellFolderViewOC. EnumDone (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841050"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="3ce4d-103">Événement ShellFolderViewOC. EnumDone</span><span class="sxs-lookup"><span data-stu-id="3ce4d-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="3ce4d-104">Indique que l’objet [**ShellFolderView**](shellfolderview.md) a terminé l’énumération du contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ce4d-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="3ce4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ce4d-106">Parameters</span></span>

<span data-ttu-id="3ce4d-107">Ce gestionnaire d’événements n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce4d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3ce4d-108">Remarks</span></span>

<span data-ttu-id="3ce4d-109">L’objet [**ShellFolderView**](shellfolderview.md) doit énumérer le contenu d’un dossier avant de pouvoir l’afficher.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="3ce4d-110">Dans le cas de dossiers volumineux ou situés sur un système distant, ce processus peut prendre plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="3ce4d-111">Pendant ce temps, un graphique Torch animé s’affiche pour indiquer à l’utilisateur que le traitement est en cours.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="3ce4d-112">Une fois l’énumération terminée, l’événement **EnumDone** est déclenché et le graphique de torche est remplacé par le contenu du dossier.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="3ce4d-113">Fournissez le code de gestion des événements pour cet événement, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="3ce4d-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="3ce4d-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3ce4d-114">Requirements</span></span>



| <span data-ttu-id="3ce4d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ce4d-115">Requirement</span></span> | <span data-ttu-id="3ce4d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ce4d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce4d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ce4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce4d-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ce4d-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ce4d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ce4d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce4d-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ce4d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3ce4d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ce4d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce4d-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce4d-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3ce4d-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="3ce4d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ce4d-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ce4d-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3ce4d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3ce4d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ce4d-126"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3ce4d-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce4d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ce4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce4d-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="3ce4d-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




