---
title: Méthode WebViewFolderContents. PopupItemMenu (shldisp. h)
description: Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Méthode PopupItemMenu fonctionnalités d’environnement Windows héritées
- Méthode PopupItemMenu fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, méthode PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740125"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="3b9d7-106">Méthode WebViewFolderContents. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="3b9d7-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="3b9d7-107">Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9d7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b9d7-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="3b9d7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b9d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b9d7-110">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b9d7-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b9d7-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="3b9d7-111">Type: **Variant**</span></span>

<span data-ttu-id="3b9d7-112">Objet [**FolderItem**](../shell/folderitem.md) pour lequel le menu contextuel sera créé.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="3b9d7-113">*VX* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3b9d7-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b9d7-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="3b9d7-114">Type: **Variant**</span></span>

<span data-ttu-id="3b9d7-115">Position horizontale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="3b9d7-116">*Vy* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3b9d7-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b9d7-117">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="3b9d7-117">Type: **Variant**</span></span>

<span data-ttu-id="3b9d7-118">Position verticale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b9d7-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b9d7-119">Return value</span></span>

<span data-ttu-id="3b9d7-120">Type : \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="3b9d7-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="3b9d7-121">Lorsque cette méthode est retournée, contient la chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="3b9d7-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="3b9d7-122">Examples</span></span>

<span data-ttu-id="3b9d7-123">L’exemple suivant illustre l’utilisation correcte de _ *PopupItemMenu*\* pour JScript Embedded en html.</span><span class="sxs-lookup"><span data-stu-id="3b9d7-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



## <a name="requirements"></a><span data-ttu-id="3b9d7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b9d7-124">Requirements</span></span>



| <span data-ttu-id="3b9d7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b9d7-125">Requirement</span></span> | <span data-ttu-id="3b9d7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b9d7-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9d7-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b9d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3b9d7-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b9d7-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3b9d7-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b9d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3b9d7-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b9d7-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b9d7-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b9d7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b9d7-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9d7-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3b9d7-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="3b9d7-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b9d7-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b9d7-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3b9d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3b9d7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b9d7-136"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3b9d7-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

