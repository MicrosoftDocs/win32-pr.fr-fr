---
description: Méthode ShellFolderView. SelectItem-définit l’état de sélection d’un élément dans la vue.
title: Méthode ShellFolderView. SelectItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116747"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="b4eff-103">Méthode ShellFolderView. SelectItem</span><span class="sxs-lookup"><span data-stu-id="b4eff-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="b4eff-104">Définit l’état de sélection d’un élément dans la vue.</span><span class="sxs-lookup"><span data-stu-id="b4eff-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4eff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4eff-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="b4eff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4eff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4eff-107">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4eff-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eff-108">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="b4eff-108">Type: **Variant\***</span></span>

<span data-ttu-id="b4eff-109">Objet [**FolderItem**](folderitem.md) pour lequel l’état de sélection sera défini.</span><span class="sxs-lookup"><span data-stu-id="b4eff-109">The [**FolderItem**](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="b4eff-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4eff-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eff-111">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="b4eff-111">Type: **Integer**</span></span>

<span data-ttu-id="b4eff-112">Ensemble d’indicateurs qui indiquent le nouvel état de sélection.</span><span class="sxs-lookup"><span data-stu-id="b4eff-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="b4eff-113">Il peut s’agir d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4eff-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="b4eff-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="b4eff-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b4eff-115">Désélectionnez l’élément.</span><span class="sxs-lookup"><span data-stu-id="b4eff-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="b4eff-116">(1)</span><span class="sxs-lookup"><span data-stu-id="b4eff-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b4eff-117">Sélectionnez l’élément.</span><span class="sxs-lookup"><span data-stu-id="b4eff-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="b4eff-118">(3)</span><span class="sxs-lookup"><span data-stu-id="b4eff-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b4eff-119">Mettez l’élément en mode édition.</span><span class="sxs-lookup"><span data-stu-id="b4eff-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="b4eff-120">(4)</span><span class="sxs-lookup"><span data-stu-id="b4eff-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b4eff-121">Désélectionner tout sauf l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4eff-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="b4eff-122">(8)</span><span class="sxs-lookup"><span data-stu-id="b4eff-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b4eff-123">Vérifiez que l’élément est affiché dans la vue.</span><span class="sxs-lookup"><span data-stu-id="b4eff-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="b4eff-124">(16)</span><span class="sxs-lookup"><span data-stu-id="b4eff-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b4eff-125">Donne le focus à l’élément.</span><span class="sxs-lookup"><span data-stu-id="b4eff-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4eff-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4eff-126">Return value</span></span>

<span data-ttu-id="b4eff-127">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b4eff-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4eff-128">Notes </span><span class="sxs-lookup"><span data-stu-id="b4eff-128">Remarks</span></span>

<span data-ttu-id="b4eff-129">[**FocusedItem**](shellfolderview-focuseditem.md) peut uniquement être appelé sur le système local.</span><span class="sxs-lookup"><span data-stu-id="b4eff-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="b4eff-130">Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="b4eff-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="b4eff-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="b4eff-131">Examples</span></span>

<span data-ttu-id="b4eff-132">L’exemple suivant illustre l’utilisation correcte de cette méthode dans JScript incorporé en HTML.</span><span class="sxs-lookup"><span data-stu-id="b4eff-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="b4eff-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4eff-133">Requirements</span></span>



| <span data-ttu-id="b4eff-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4eff-134">Requirement</span></span> | <span data-ttu-id="b4eff-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4eff-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eff-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4eff-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b4eff-137">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4eff-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b4eff-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4eff-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b4eff-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4eff-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4eff-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4eff-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4eff-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4eff-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b4eff-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="b4eff-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4eff-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4eff-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b4eff-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b4eff-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4eff-145"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b4eff-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




