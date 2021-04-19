---
title: Méthode WebViewFolderContents. SelectItem (shldisp. h)
description: Définit l’état de sélection d’un élément dans la vue.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Méthode SelectItem fonctionnalités d’environnement Windows héritées
- Méthode SelectItem fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, méthode SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511734"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="9c43e-106">Méthode WebViewFolderContents. SelectItem</span><span class="sxs-lookup"><span data-stu-id="9c43e-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="9c43e-107">Définit l’état de sélection d’un élément dans la vue.</span><span class="sxs-lookup"><span data-stu-id="9c43e-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c43e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c43e-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="9c43e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c43e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c43e-110">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c43e-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c43e-111">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="9c43e-111">Type: \**Variant\** _</span></span>

<span data-ttu-id="9c43e-112">Objet [_ *FolderItem* \*](../shell/folderitem.md) pour lequel l’état de sélection sera défini.</span><span class="sxs-lookup"><span data-stu-id="9c43e-112">The [_ *FolderItem*\*](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="9c43e-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c43e-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c43e-114">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="9c43e-114">Type: **Integer**</span></span>

<span data-ttu-id="9c43e-115">Ensemble d’indicateurs qui indiquent le nouvel état de sélection.</span><span class="sxs-lookup"><span data-stu-id="9c43e-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="9c43e-116">Il peut s’agir d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9c43e-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="9c43e-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="9c43e-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9c43e-118">Désélectionnez l’élément.</span><span class="sxs-lookup"><span data-stu-id="9c43e-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="9c43e-119">(1)</span><span class="sxs-lookup"><span data-stu-id="9c43e-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9c43e-120">Sélectionnez l’élément.</span><span class="sxs-lookup"><span data-stu-id="9c43e-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="9c43e-121">(3)</span><span class="sxs-lookup"><span data-stu-id="9c43e-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9c43e-122">Mettez l’élément en mode édition.</span><span class="sxs-lookup"><span data-stu-id="9c43e-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="9c43e-123">(4)</span><span class="sxs-lookup"><span data-stu-id="9c43e-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9c43e-124">Désélectionner tout sauf l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="9c43e-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="9c43e-125">(8)</span><span class="sxs-lookup"><span data-stu-id="9c43e-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9c43e-126">Vérifiez que l’élément est affiché dans la vue.</span><span class="sxs-lookup"><span data-stu-id="9c43e-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="9c43e-127">(16)</span><span class="sxs-lookup"><span data-stu-id="9c43e-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9c43e-128">Donne le focus à l’élément.</span><span class="sxs-lookup"><span data-stu-id="9c43e-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c43e-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9c43e-129">Return value</span></span>

<span data-ttu-id="9c43e-130">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9c43e-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="9c43e-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="9c43e-131">Examples</span></span>

<span data-ttu-id="9c43e-132">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="9c43e-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



## <a name="requirements"></a><span data-ttu-id="9c43e-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c43e-133">Requirements</span></span>



| <span data-ttu-id="9c43e-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c43e-134">Requirement</span></span> | <span data-ttu-id="9c43e-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c43e-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c43e-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c43e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9c43e-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c43e-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9c43e-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c43e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9c43e-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c43e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c43e-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c43e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c43e-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c43e-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9c43e-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="9c43e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c43e-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c43e-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9c43e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9c43e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c43e-145"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9c43e-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

