---
description: Actualise le contenu du menu Démarrer. Utilisé uniquement avec les systèmes antérieurs à Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Shell. RefreshMenu, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973255"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="725de-104">Shell. RefreshMenu, méthode</span><span class="sxs-lookup"><span data-stu-id="725de-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="725de-105">Actualise le contenu du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="725de-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="725de-106">Utilisé uniquement avec les systèmes antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="725de-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="725de-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="725de-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="725de-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="725de-108">Parameters</span></span>

<span data-ttu-id="725de-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="725de-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="725de-110">Notes</span><span class="sxs-lookup"><span data-stu-id="725de-110">Remarks</span></span>

<span data-ttu-id="725de-111">La fonctionnalité fournie par **RefreshMenu** est gérée automatiquement sous Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="725de-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="725de-112">N’appelez pas cette méthode sous ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="725de-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="725de-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="725de-113">Examples</span></span>

<span data-ttu-id="725de-114">L’exemple suivant montre **RefreshMenu** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="725de-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="725de-115">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="725de-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="725de-116">Langage</span><span class="sxs-lookup"><span data-stu-id="725de-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="725de-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="725de-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="725de-118">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="725de-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="725de-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="725de-119">Requirements</span></span>



| <span data-ttu-id="725de-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="725de-120">Requirement</span></span> | <span data-ttu-id="725de-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="725de-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="725de-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="725de-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725de-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="725de-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="725de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="725de-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="725de-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="725de-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="725de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="725de-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="725de-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="725de-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="725de-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="725de-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="725de-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="725de-130">DLL</span><span class="sxs-lookup"><span data-stu-id="725de-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="725de-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="725de-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




