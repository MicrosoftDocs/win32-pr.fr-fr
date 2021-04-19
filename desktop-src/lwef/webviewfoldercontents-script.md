---
title: WebViewFolderContents. script, propriété (shldisp. h)
description: Obtient l’objet de script pour la vue.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Propriétés de script héritées fonctionnalités d’environnement Windows
- Propriétés de script héritées fonctionnalités de l’environnement Windows, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, propriété de script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513631"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="9de93-106">WebViewFolderContents. script, propriété</span><span class="sxs-lookup"><span data-stu-id="9de93-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="9de93-107">Obtient l’objet de script pour la vue.</span><span class="sxs-lookup"><span data-stu-id="9de93-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="9de93-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9de93-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de93-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9de93-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="9de93-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9de93-110">Property value</span></span>

<span data-ttu-id="9de93-111">Variable de type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet de script.</span><span class="sxs-lookup"><span data-stu-id="9de93-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="9de93-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="9de93-112">Examples</span></span>

<span data-ttu-id="9de93-113">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="9de93-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
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



## <a name="requirements"></a><span data-ttu-id="9de93-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9de93-114">Requirements</span></span>



| <span data-ttu-id="9de93-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9de93-115">Requirement</span></span> | <span data-ttu-id="9de93-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9de93-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de93-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9de93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9de93-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9de93-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9de93-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9de93-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9de93-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9de93-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9de93-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9de93-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de93-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de93-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9de93-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="9de93-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9de93-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9de93-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9de93-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9de93-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9de93-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9de93-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

