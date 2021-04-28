---
title: WebViewFolderContents.SelectedItems, méthode (Shldisp.h)
description: WebViewFolderContents. SelectedItems, méthode-obtient un objet FolderItems qui représente tous les éléments sélectionnés dans la vue.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- SelectedItems, méthode fonctionnalités d’environnement Windows héritées
- SelectedItems, méthode fonctionnalités d’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, SelectedItems, méthode
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102647"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="1617b-106">WebViewFolderContents. SelectedItems, méthode</span><span class="sxs-lookup"><span data-stu-id="1617b-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="1617b-107">Obtient un objet [**FolderItems**](../shell/folderitems.md) qui représente tous les éléments sélectionnés dans la vue.</span><span class="sxs-lookup"><span data-stu-id="1617b-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="1617b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1617b-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="1617b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1617b-109">Parameters</span></span>

<span data-ttu-id="1617b-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1617b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1617b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1617b-111">Return value</span></span>

<span data-ttu-id="1617b-112">Type : **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1617b-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="1617b-113">Référence d’objet à l’objet [**FolderItems**](../shell/folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="1617b-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="1617b-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="1617b-114">Examples</span></span>

<span data-ttu-id="1617b-115">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="1617b-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



## <a name="requirements"></a><span data-ttu-id="1617b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1617b-116">Requirements</span></span>



| <span data-ttu-id="1617b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1617b-117">Requirement</span></span> | <span data-ttu-id="1617b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1617b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1617b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1617b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1617b-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1617b-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1617b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1617b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1617b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1617b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1617b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1617b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1617b-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1617b-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1617b-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="1617b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1617b-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1617b-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1617b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1617b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1617b-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1617b-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

