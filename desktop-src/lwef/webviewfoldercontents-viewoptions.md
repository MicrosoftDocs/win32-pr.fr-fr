---
title: WebViewFolderContents. ViewOptions, propriété (shldisp. h)
description: Obtient un jeu d’indicateurs ShellFolderViewOptions qui indiquent les options actuelles de la vue.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Propriétés ViewOptions héritées fonctionnalités de l’environnement Windows
- Propriété ViewOptions fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, propriété ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032446"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="1ae5a-106">WebViewFolderContents. ViewOptions, propriété</span><span class="sxs-lookup"><span data-stu-id="1ae5a-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="1ae5a-107">Obtient un jeu d’indicateurs [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) qui indiquent les options actuelles de la vue.</span><span class="sxs-lookup"><span data-stu-id="1ae5a-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="1ae5a-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1ae5a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae5a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ae5a-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="1ae5a-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1ae5a-110">Property value</span></span>

<span data-ttu-id="1ae5a-111">Variable de type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet d’options de vue.</span><span class="sxs-lookup"><span data-stu-id="1ae5a-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="1ae5a-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="1ae5a-112">Examples</span></span>

<span data-ttu-id="1ae5a-113">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="1ae5a-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="1ae5a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ae5a-114">Requirements</span></span>



| <span data-ttu-id="1ae5a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ae5a-115">Requirement</span></span> | <span data-ttu-id="1ae5a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ae5a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae5a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae5a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae5a-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ae5a-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1ae5a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae5a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae5a-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ae5a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ae5a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ae5a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae5a-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae5a-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1ae5a-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="1ae5a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ae5a-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ae5a-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1ae5a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1ae5a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ae5a-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1ae5a-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

