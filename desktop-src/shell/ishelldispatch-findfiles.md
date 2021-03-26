---
description: 'Affiche la boîte de dialogue Rechercher : tous les fichiers. Cela revient à cliquer sur le menu Démarrer, puis à sélectionner Rechercher.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Méthode IShellDispatch. FindFiles (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863146"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="c9163-104">Méthode IShellDispatch. FindFiles</span><span class="sxs-lookup"><span data-stu-id="c9163-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="c9163-105">Affiche la boîte de dialogue **Rechercher : tous les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="c9163-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="c9163-106">Cela revient à cliquer sur le menu **Démarrer** , puis à sélectionner **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="c9163-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9163-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9163-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="c9163-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9163-108">Parameters</span></span>

<span data-ttu-id="c9163-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c9163-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9163-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9163-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c9163-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c9163-111">JScript</span></span>

<span data-ttu-id="c9163-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c9163-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c9163-113">VB</span><span class="sxs-lookup"><span data-stu-id="c9163-113">VB</span></span>

<span data-ttu-id="c9163-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c9163-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9163-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c9163-115">Remarks</span></span>

<span data-ttu-id="c9163-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FindFiles**](shell-findfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="c9163-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c9163-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c9163-117">Examples</span></span>

<span data-ttu-id="c9163-118">Les exemples suivants illustrent l’utilisation de **FindFiles** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c9163-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c9163-119">Langage</span><span class="sxs-lookup"><span data-stu-id="c9163-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="c9163-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="c9163-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="c9163-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c9163-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c9163-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9163-122">Requirements</span></span>



| <span data-ttu-id="c9163-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9163-123">Requirement</span></span> | <span data-ttu-id="c9163-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9163-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9163-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9163-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c9163-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9163-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c9163-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9163-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c9163-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9163-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9163-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9163-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9163-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9163-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c9163-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="c9163-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9163-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9163-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c9163-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c9163-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9163-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c9163-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




