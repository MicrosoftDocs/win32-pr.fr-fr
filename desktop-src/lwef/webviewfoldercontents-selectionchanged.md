---
title: Événement WebViewFolderContents. SelectionChanged (shldisp. h)
description: Événement WebViewFolderContents. SelectionChanged-se produit lorsque l’état de sélection de tous les éléments de la vue a changé.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- Fonctionnalités de l’environnement Windows hérité des événements SelectionChanged
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6176cb2a1703d48cd2ddec8069c65d7efc978f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102657"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="69b41-104">Événement WebViewFolderContents. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="69b41-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="69b41-105">Se produit lorsque l’état de sélection d’un élément ou d’éléments de la vue a été modifié.</span><span class="sxs-lookup"><span data-stu-id="69b41-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b41-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69b41-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="69b41-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69b41-107">Parameters</span></span>

<span data-ttu-id="69b41-108">Ce gestionnaire d’événements n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="69b41-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="69b41-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="69b41-109">Examples</span></span>

<span data-ttu-id="69b41-110">L’exemple suivant illustre l’utilisation correcte de cet événement pour JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="69b41-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="69b41-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69b41-111">Requirements</span></span>



| <span data-ttu-id="69b41-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69b41-112">Requirement</span></span> | <span data-ttu-id="69b41-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="69b41-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b41-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69b41-114">Minimum supported client</span></span><br/> | <span data-ttu-id="69b41-115">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69b41-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="69b41-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69b41-116">Minimum supported server</span></span><br/> | <span data-ttu-id="69b41-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69b41-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69b41-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="69b41-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b41-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b41-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="69b41-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="69b41-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69b41-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="69b41-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="69b41-122">DLL</span><span class="sxs-lookup"><span data-stu-id="69b41-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69b41-123"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="69b41-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





