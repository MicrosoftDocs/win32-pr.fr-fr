---
description: Mosaïques horizontalement toutes les fenêtres sur le bureau. Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option Afficher les fenêtres empilées.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Méthode IShellDispatch. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113975"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="2c169-104">Méthode IShellDispatch. TileHorizontally</span><span class="sxs-lookup"><span data-stu-id="2c169-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="2c169-105">Mosaïques horizontalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="2c169-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="2c169-106">Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option **afficher les fenêtres empilées**.</span><span class="sxs-lookup"><span data-stu-id="2c169-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c169-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c169-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="2c169-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c169-108">Parameters</span></span>

<span data-ttu-id="2c169-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2c169-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c169-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c169-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2c169-111">JScript</span><span class="sxs-lookup"><span data-stu-id="2c169-111">JScript</span></span>

<span data-ttu-id="2c169-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2c169-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2c169-113">VB</span><span class="sxs-lookup"><span data-stu-id="2c169-113">VB</span></span>

<span data-ttu-id="2c169-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2c169-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c169-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2c169-115">Remarks</span></span>

<span data-ttu-id="2c169-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. TileHorizontally**](shell-tilehorizontally.md) .</span><span class="sxs-lookup"><span data-stu-id="2c169-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2c169-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="2c169-117">Examples</span></span>

<span data-ttu-id="2c169-118">L’exemple suivant illustre l’utilisation de **TileHorizontally** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2c169-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2c169-119">Langage</span><span class="sxs-lookup"><span data-stu-id="2c169-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="2c169-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="2c169-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2c169-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="2c169-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2c169-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c169-122">Requirements</span></span>



| <span data-ttu-id="2c169-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c169-123">Requirement</span></span> | <span data-ttu-id="2c169-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c169-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c169-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c169-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2c169-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c169-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2c169-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c169-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2c169-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c169-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c169-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c169-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c169-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c169-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2c169-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="2c169-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c169-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c169-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2c169-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2c169-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c169-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2c169-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




