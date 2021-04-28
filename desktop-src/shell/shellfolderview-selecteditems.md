---
description: ShellFolderView. SelectedItems, méthode-obtient un objet FolderItems qui représente tous les éléments sélectionnés dans la vue.
title: ShellFolderView. SelectedItems, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: 54cf67f1b75ae9d6423b02d0cacdde032ad2e018
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083377"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="5df4d-103">ShellFolderView. SelectedItems, méthode</span><span class="sxs-lookup"><span data-stu-id="5df4d-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="5df4d-104">Obtient un objet [**FolderItems**](folderitems.md) qui représente tous les éléments sélectionnés dans la vue.</span><span class="sxs-lookup"><span data-stu-id="5df4d-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5df4d-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="5df4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5df4d-106">Parameters</span></span>

<span data-ttu-id="5df4d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5df4d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5df4d-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5df4d-108">Return value</span></span>

<span data-ttu-id="5df4d-109">Type : **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5df4d-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="5df4d-110">Référence d’objet à l’objet [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="5df4d-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df4d-111">Notes </span><span class="sxs-lookup"><span data-stu-id="5df4d-111">Remarks</span></span>

<span data-ttu-id="5df4d-112">**SelectedItems** ne peut être appelé que sur le système local.</span><span class="sxs-lookup"><span data-stu-id="5df4d-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="5df4d-113">Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="5df4d-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="5df4d-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="5df4d-114">Examples</span></span>

<span data-ttu-id="5df4d-115">L’exemple suivant illustre l’utilisation correcte de cette méthode dans JScript incorporé en HTML.</span><span class="sxs-lookup"><span data-stu-id="5df4d-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="5df4d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5df4d-116">Requirements</span></span>



| <span data-ttu-id="5df4d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5df4d-117">Requirement</span></span> | <span data-ttu-id="5df4d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5df4d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df4d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5df4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5df4d-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5df4d-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5df4d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5df4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5df4d-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5df4d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5df4d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5df4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df4d-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df4d-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5df4d-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="5df4d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5df4d-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5df4d-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5df4d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5df4d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5df4d-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5df4d-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




