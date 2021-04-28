---
title: Méthode WebViewFolderContents. SelectItem (shldisp. h)
description: Méthode WebViewFolderContents. SelectItem-définit l’état de sélection d’un élément dans la vue.
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
ms.openlocfilehash: 66e2d05c010199f05826df7ed4591e8c7c1723e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102608"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="8750d-106">Méthode WebViewFolderContents. SelectItem</span><span class="sxs-lookup"><span data-stu-id="8750d-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="8750d-107">Définit l’état de sélection d’un élément dans la vue.</span><span class="sxs-lookup"><span data-stu-id="8750d-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="8750d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8750d-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="8750d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8750d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8750d-110">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8750d-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8750d-111">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="8750d-111">Type: **Variant\***</span></span>

<span data-ttu-id="8750d-112">Objet [**FolderItem**](../shell/folderitem.md) pour lequel l’état de sélection sera défini.</span><span class="sxs-lookup"><span data-stu-id="8750d-112">The [**FolderItem**](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="8750d-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8750d-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8750d-114">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="8750d-114">Type: **Integer**</span></span>

<span data-ttu-id="8750d-115">Ensemble d’indicateurs qui indiquent le nouvel état de sélection.</span><span class="sxs-lookup"><span data-stu-id="8750d-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="8750d-116">Il peut s’agir d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8750d-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="8750d-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="8750d-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8750d-118">Désélectionnez l’élément.</span><span class="sxs-lookup"><span data-stu-id="8750d-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8750d-119">(1)</span><span class="sxs-lookup"><span data-stu-id="8750d-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8750d-120">Sélectionnez l’élément.</span><span class="sxs-lookup"><span data-stu-id="8750d-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8750d-121">(3)</span><span class="sxs-lookup"><span data-stu-id="8750d-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8750d-122">Mettez l’élément en mode édition.</span><span class="sxs-lookup"><span data-stu-id="8750d-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="8750d-123">(4)</span><span class="sxs-lookup"><span data-stu-id="8750d-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8750d-124">Désélectionner tout sauf l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="8750d-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="8750d-125">(8)</span><span class="sxs-lookup"><span data-stu-id="8750d-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8750d-126">Vérifiez que l’élément est affiché dans la vue.</span><span class="sxs-lookup"><span data-stu-id="8750d-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="8750d-127">(16)</span><span class="sxs-lookup"><span data-stu-id="8750d-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8750d-128">Donne le focus à l’élément.</span><span class="sxs-lookup"><span data-stu-id="8750d-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8750d-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8750d-129">Return value</span></span>

<span data-ttu-id="8750d-130">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8750d-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8750d-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="8750d-131">Examples</span></span>

<span data-ttu-id="8750d-132">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="8750d-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8750d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8750d-133">Requirements</span></span>



| <span data-ttu-id="8750d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8750d-134">Requirement</span></span> | <span data-ttu-id="8750d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8750d-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8750d-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8750d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8750d-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8750d-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8750d-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8750d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8750d-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8750d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8750d-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="8750d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8750d-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8750d-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8750d-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="8750d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8750d-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8750d-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8750d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8750d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8750d-145"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8750d-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

