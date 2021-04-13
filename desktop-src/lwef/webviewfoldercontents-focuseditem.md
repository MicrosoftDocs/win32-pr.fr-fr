---
title: WebViewFolderContents. FocusedItem, propriété (shldisp. h)
description: Obtient un objet FolderItem qui représente l’élément ayant le focus d’entrée.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Propriétés FocusedItem héritées fonctionnalités de l’environnement Windows
- Propriété FocusedItem fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, propriété FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e7c2a4c280a949ec3684e2b05610830315a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383943"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="e9435-106">WebViewFolderContents. FocusedItem, propriété</span><span class="sxs-lookup"><span data-stu-id="e9435-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="e9435-107">Obtient un objet [**FolderItem**](../shell/folderitem.md) qui représente l’élément ayant le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e9435-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="e9435-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e9435-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9435-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9435-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="e9435-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e9435-110">Property value</span></span>

<span data-ttu-id="e9435-111">Variable de type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet élément ayant le focus.</span><span class="sxs-lookup"><span data-stu-id="e9435-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="e9435-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="e9435-112">Examples</span></span>

<span data-ttu-id="e9435-113">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="e9435-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="e9435-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9435-114">Requirements</span></span>



| <span data-ttu-id="e9435-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9435-115">Requirement</span></span> | <span data-ttu-id="e9435-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9435-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9435-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9435-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9435-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9435-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e9435-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9435-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9435-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9435-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9435-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9435-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9435-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9435-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e9435-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="e9435-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9435-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9435-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e9435-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e9435-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9435-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e9435-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

