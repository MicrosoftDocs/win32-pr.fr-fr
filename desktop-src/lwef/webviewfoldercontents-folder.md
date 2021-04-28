---
title: WebViewFolderContents.Folder, propriété (Shldisp.h)
description: WebViewFolderContents. Folder, propriété-obtient un objet Folder qui représente la vue.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Propriétés du dossier fonctionnalités d’environnement Windows héritées
- Propriété de dossier fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objets WebViewFolderContents hérités fonctionnalités de l’environnement Windows, propriété de dossier
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102697"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="63622-106">WebViewFolderContents. Folder, propriété</span><span class="sxs-lookup"><span data-stu-id="63622-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="63622-107">Obtient un objet [**dossier**](../shell/folder.md) qui représente la vue.</span><span class="sxs-lookup"><span data-stu-id="63622-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="63622-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="63622-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63622-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63622-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="63622-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="63622-110">Property value</span></span>

<span data-ttu-id="63622-111">Objet qui reçoit l’objet [**Folder**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="63622-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="63622-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="63622-112">Examples</span></span>

<span data-ttu-id="63622-113">L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="63622-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



## <a name="requirements"></a><span data-ttu-id="63622-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63622-114">Requirements</span></span>



| <span data-ttu-id="63622-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63622-115">Requirement</span></span> | <span data-ttu-id="63622-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="63622-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63622-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63622-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63622-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63622-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="63622-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63622-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63622-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63622-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63622-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="63622-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="63622-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63622-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="63622-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="63622-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63622-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63622-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="63622-125">DLL</span><span class="sxs-lookup"><span data-stu-id="63622-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63622-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="63622-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

