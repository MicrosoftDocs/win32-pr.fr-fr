---
description: Mosaïque verticalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option Afficher les fenêtres côte à côte.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Méthode IShellDispatch. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972411"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="feaf2-104">Méthode IShellDispatch. TileVertically</span><span class="sxs-lookup"><span data-stu-id="feaf2-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="feaf2-105">Mosaïque verticalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="feaf2-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="feaf2-106">Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option **afficher les fenêtres côte à côte**.</span><span class="sxs-lookup"><span data-stu-id="feaf2-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="feaf2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="feaf2-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="feaf2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="feaf2-108">Parameters</span></span>

<span data-ttu-id="feaf2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="feaf2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="feaf2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="feaf2-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="feaf2-111">JScript</span><span class="sxs-lookup"><span data-stu-id="feaf2-111">JScript</span></span>

<span data-ttu-id="feaf2-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="feaf2-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="feaf2-113">VB</span><span class="sxs-lookup"><span data-stu-id="feaf2-113">VB</span></span>

<span data-ttu-id="feaf2-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="feaf2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="feaf2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="feaf2-115">Remarks</span></span>

<span data-ttu-id="feaf2-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. TileVertically**](shell-tilevertically.md) .</span><span class="sxs-lookup"><span data-stu-id="feaf2-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="feaf2-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="feaf2-117">Examples</span></span>

<span data-ttu-id="feaf2-118">Les exemples suivants illustrent l’utilisation de **TileVertically** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="feaf2-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="feaf2-119">Langage</span><span class="sxs-lookup"><span data-stu-id="feaf2-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="feaf2-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="feaf2-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="feaf2-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="feaf2-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="feaf2-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="feaf2-122">Requirements</span></span>



| <span data-ttu-id="feaf2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="feaf2-123">Requirement</span></span> | <span data-ttu-id="feaf2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="feaf2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feaf2-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="feaf2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="feaf2-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="feaf2-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="feaf2-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="feaf2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="feaf2-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="feaf2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="feaf2-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="feaf2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="feaf2-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="feaf2-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="feaf2-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="feaf2-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="feaf2-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="feaf2-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="feaf2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="feaf2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feaf2-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="feaf2-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




