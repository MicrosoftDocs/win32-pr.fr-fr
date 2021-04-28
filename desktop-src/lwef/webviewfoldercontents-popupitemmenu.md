---
title: Méthode WebViewFolderContents. PopupItemMenu (shldisp. h)
description: 'Méthode WebViewFolderContents. PopupItemMenu : crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.'
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
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102637"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="129cc-106">Méthode WebViewFolderContents. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="129cc-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="129cc-107">Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="129cc-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="129cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="129cc-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="129cc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="129cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129cc-110">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="129cc-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="129cc-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="129cc-111">Type: **Variant**</span></span>

<span data-ttu-id="129cc-112">Objet [**FolderItem**](../shell/folderitem.md) pour lequel le menu contextuel sera créé.</span><span class="sxs-lookup"><span data-stu-id="129cc-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="129cc-113">*VX* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="129cc-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="129cc-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="129cc-114">Type: **Variant**</span></span>

<span data-ttu-id="129cc-115">Position horizontale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="129cc-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="129cc-116">*Vy* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="129cc-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="129cc-117">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="129cc-117">Type: **Variant**</span></span>

<span data-ttu-id="129cc-118">Position verticale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="129cc-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129cc-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="129cc-119">Return value</span></span>

<span data-ttu-id="129cc-120">Type : **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="129cc-120">Type: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="129cc-121">Lorsque cette méthode est retournée, contient la chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="129cc-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="129cc-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="129cc-122">Examples</span></span>

<span data-ttu-id="129cc-123">L’exemple suivant illustre l’utilisation correcte de **PopupItemMenu** pour JScript Embedded en html.</span><span class="sxs-lookup"><span data-stu-id="129cc-123">The following example shows the proper use of **PopupItemMenu** for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="129cc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="129cc-124">Requirements</span></span>



| <span data-ttu-id="129cc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="129cc-125">Requirement</span></span> | <span data-ttu-id="129cc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="129cc-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="129cc-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="129cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="129cc-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="129cc-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="129cc-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="129cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="129cc-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="129cc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="129cc-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="129cc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="129cc-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="129cc-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="129cc-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="129cc-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="129cc-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="129cc-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="129cc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="129cc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="129cc-136"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="129cc-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

