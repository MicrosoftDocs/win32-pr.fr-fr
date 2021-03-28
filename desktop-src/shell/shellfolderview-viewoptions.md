---
description: Obtient un jeu d’indicateurs qui indiquent les options actuelles de la vue.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: ShellFolderView. ViewOptions, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991720"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="05da5-103">ShellFolderView. ViewOptions, propriété</span><span class="sxs-lookup"><span data-stu-id="05da5-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="05da5-104">Obtient un jeu d’indicateurs qui indiquent les options actuelles de la vue.</span><span class="sxs-lookup"><span data-stu-id="05da5-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="05da5-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="05da5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05da5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05da5-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="05da5-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="05da5-107">Property value</span></span>

<span data-ttu-id="05da5-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet d’options de vue.</span><span class="sxs-lookup"><span data-stu-id="05da5-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="05da5-109">Contient une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="05da5-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="05da5-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="05da5-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-111">L’option **Afficher tous les fichiers** est activée.</span><span class="sxs-lookup"><span data-stu-id="05da5-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="05da5-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="05da5-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-113">L’option **Masquer les extensions pour les types de fichiers connus** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="05da5-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="05da5-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="05da5-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-115">L’option **afficher les fichiers et les dossiers compressés avec une autre couleur** est activée.</span><span class="sxs-lookup"><span data-stu-id="05da5-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="05da5-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="05da5-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-117">L’option **ne pas afficher les fichiers masqués** est activée.</span><span class="sxs-lookup"><span data-stu-id="05da5-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="05da5-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_ WIN95CLASSIC** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="05da5-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-119">L’option de **style classique** est activée.</span><span class="sxs-lookup"><span data-stu-id="05da5-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="05da5-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="05da5-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-121">Le **double-clic pour ouvrir une** option d’élément est activé.</span><span class="sxs-lookup"><span data-stu-id="05da5-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="05da5-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="05da5-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="05da5-123">L’option **Active Desktop – afficher en tant que page Web** est activée.</span><span class="sxs-lookup"><span data-stu-id="05da5-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05da5-124">Notes</span><span class="sxs-lookup"><span data-stu-id="05da5-124">Remarks</span></span>

<span data-ttu-id="05da5-125">[**FocusedItem**](shellfolderview-focuseditem.md) peut uniquement être appelé sur le système local.</span><span class="sxs-lookup"><span data-stu-id="05da5-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="05da5-126">Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="05da5-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="05da5-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="05da5-127">Examples</span></span>

<span data-ttu-id="05da5-128">L’exemple suivant illustre l’utilisation correcte de cette méthode dans JScript incorporé en HTML.</span><span class="sxs-lookup"><span data-stu-id="05da5-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
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
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="05da5-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="05da5-129">Requirements</span></span>



| <span data-ttu-id="05da5-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05da5-130">Requirement</span></span> | <span data-ttu-id="05da5-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="05da5-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05da5-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05da5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05da5-133">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05da5-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="05da5-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05da5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05da5-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05da5-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05da5-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="05da5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="05da5-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05da5-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="05da5-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="05da5-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05da5-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05da5-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="05da5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="05da5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05da5-141"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="05da5-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
