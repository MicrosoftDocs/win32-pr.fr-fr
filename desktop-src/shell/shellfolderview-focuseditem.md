---
description: Propriété ShellFolderView. FocusedItem-obtient un objet FolderItem qui représente l’élément ayant le focus d’entrée.
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: ShellFolderView. FocusedItem, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4f661f555f1492a3323fa3749a8dffd6f00f411d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104007"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="42364-103">ShellFolderView. FocusedItem, propriété</span><span class="sxs-lookup"><span data-stu-id="42364-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="42364-104">Obtient un objet [**FolderItem**](folderitem.md) qui représente l’élément ayant le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="42364-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="42364-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="42364-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42364-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42364-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="42364-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="42364-107">Property value</span></span>

<span data-ttu-id="42364-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet élément ayant le focus.</span><span class="sxs-lookup"><span data-stu-id="42364-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="42364-109">Notes </span><span class="sxs-lookup"><span data-stu-id="42364-109">Remarks</span></span>

<span data-ttu-id="42364-110">**FocusedItem** peut uniquement être appelé sur le système local.</span><span class="sxs-lookup"><span data-stu-id="42364-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="42364-111">Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="42364-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="42364-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="42364-112">Examples</span></span>

<span data-ttu-id="42364-113">L’exemple suivant illustre l’utilisation correcte de cette méthode dans JScript incorporé en HTML.</span><span class="sxs-lookup"><span data-stu-id="42364-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
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
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="42364-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42364-114">Requirements</span></span>



| <span data-ttu-id="42364-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42364-115">Requirement</span></span> | <span data-ttu-id="42364-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="42364-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42364-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42364-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42364-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42364-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42364-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42364-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42364-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42364-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42364-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="42364-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42364-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42364-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="42364-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="42364-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42364-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42364-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="42364-125">DLL</span><span class="sxs-lookup"><span data-stu-id="42364-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42364-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="42364-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
