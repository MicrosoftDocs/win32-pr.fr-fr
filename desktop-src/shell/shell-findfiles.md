---
description: 'Affiche la boîte de dialogue Rechercher : tous les fichiers. Cela revient à cliquer sur le menu Démarrer, puis à sélectionner Rechercher (ou son équivalent sous systèmes antérieurs à Windows XP).'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Shell. FindFiles, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209947"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="d6019-104">Shell. FindFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="d6019-104">Shell.FindFiles method</span></span>

<span data-ttu-id="d6019-105">Affiche la boîte de dialogue **Rechercher : tous les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="d6019-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="d6019-106">Cela revient à cliquer sur le menu **Démarrer** , puis à sélectionner **Rechercher** (ou son équivalent sous systèmes ANTÉRIEURs à Windows XP).</span><span class="sxs-lookup"><span data-stu-id="d6019-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6019-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6019-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="d6019-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6019-108">Parameters</span></span>

<span data-ttu-id="d6019-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d6019-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6019-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6019-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d6019-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d6019-111">JScript</span></span>

<span data-ttu-id="d6019-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d6019-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d6019-113">VB</span><span class="sxs-lookup"><span data-stu-id="d6019-113">VB</span></span>

<span data-ttu-id="d6019-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d6019-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d6019-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="d6019-115">Examples</span></span>

<span data-ttu-id="d6019-116">L’exemple suivant montre **FindFiles** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d6019-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="d6019-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d6019-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d6019-118">Langage</span><span class="sxs-lookup"><span data-stu-id="d6019-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="d6019-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="d6019-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d6019-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="d6019-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d6019-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6019-121">Requirements</span></span>



| <span data-ttu-id="d6019-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6019-122">Requirement</span></span> | <span data-ttu-id="d6019-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6019-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6019-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6019-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6019-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6019-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d6019-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6019-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6019-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6019-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6019-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6019-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6019-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6019-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d6019-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="d6019-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6019-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6019-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d6019-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d6019-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6019-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d6019-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




