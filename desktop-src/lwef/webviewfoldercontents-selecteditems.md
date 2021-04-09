---
title: WebViewFolderContents.SelectedItems, méthode (Shldisp.h)
description: Obtient un objet FolderItems qui représente tous les éléments sélectionnés dans la vue.
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
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033169"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="6bdad-106">WebViewFolderContents. SelectedItems, méthode</span><span class="sxs-lookup"><span data-stu-id="6bdad-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="6bdad-107">Obtient un objet [**FolderItems**](../shell/folderitems.md) qui représente tous les éléments sélectionnés dans la vue.</span><span class="sxs-lookup"><span data-stu-id="6bdad-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bdad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bdad-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="6bdad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bdad-109">Parameters</span></span>

<span data-ttu-id="6bdad-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6bdad-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bdad-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6bdad-111">Return value</span></span>

<span data-ttu-id="6bdad-112">Type : **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6bdad-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="6bdad-113">Référence d’objet à l’objet [**FolderItems**](../shell/folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="6bdad-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="6bdad-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="6bdad-114">Examples</span></span>

<span data-ttu-id="6bdad-115">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="6bdad-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6bdad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bdad-116">Requirements</span></span>



| <span data-ttu-id="6bdad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bdad-117">Requirement</span></span> | <span data-ttu-id="6bdad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bdad-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdad-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bdad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6bdad-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bdad-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6bdad-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bdad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6bdad-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bdad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6bdad-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="6bdad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bdad-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bdad-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6bdad-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="6bdad-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6bdad-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6bdad-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6bdad-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6bdad-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bdad-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6bdad-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

