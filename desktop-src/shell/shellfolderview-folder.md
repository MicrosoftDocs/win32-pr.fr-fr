---
description: ShellFolderView. Folder, propriété-obtient un objet Folder qui représente la vue.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: ShellFolderView. Folder, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 370fddc1428c8f77edb77cdac2dc04123fc5211f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083417"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="b3916-103">ShellFolderView. Folder, propriété</span><span class="sxs-lookup"><span data-stu-id="b3916-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="b3916-104">Obtient un objet [**dossier**](folder.md) qui représente la vue.</span><span class="sxs-lookup"><span data-stu-id="b3916-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="b3916-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b3916-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3916-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3916-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="b3916-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b3916-107">Property value</span></span>

<span data-ttu-id="b3916-108">Objet qui reçoit l’objet [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="b3916-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3916-109">Notes </span><span class="sxs-lookup"><span data-stu-id="b3916-109">Remarks</span></span>

<span data-ttu-id="b3916-110">Le **dossier** ne peut être appelé que sur le système local.</span><span class="sxs-lookup"><span data-stu-id="b3916-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="b3916-111">Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="b3916-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="b3916-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="b3916-112">Examples</span></span>

<span data-ttu-id="b3916-113">L’exemple suivant illustre l’utilisation correcte de cette propriété pour JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="b3916-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="b3916-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3916-114">Requirements</span></span>



| <span data-ttu-id="b3916-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3916-115">Requirement</span></span> | <span data-ttu-id="b3916-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3916-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3916-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3916-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b3916-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3916-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b3916-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3916-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b3916-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3916-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b3916-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3916-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3916-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3916-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b3916-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="b3916-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3916-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3916-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b3916-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b3916-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3916-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b3916-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




