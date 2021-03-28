---
description: 'Affiche la boîte de dialogue résultats de la recherche : ordinateurs. La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Shell. FindComputer, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973694"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="1845d-104">Shell. FindComputer, méthode</span><span class="sxs-lookup"><span data-stu-id="1845d-104">Shell.FindComputer method</span></span>

<span data-ttu-id="1845d-105">Affiche la boîte de dialogue résultats de la **recherche : ordinateurs** .</span><span class="sxs-lookup"><span data-stu-id="1845d-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="1845d-106">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1845d-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1845d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1845d-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="1845d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1845d-108">Parameters</span></span>

<span data-ttu-id="1845d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1845d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1845d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1845d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1845d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1845d-111">JScript</span></span>

<span data-ttu-id="1845d-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1845d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1845d-113">VB</span><span class="sxs-lookup"><span data-stu-id="1845d-113">VB</span></span>

<span data-ttu-id="1845d-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1845d-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="1845d-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="1845d-115">Examples</span></span>

<span data-ttu-id="1845d-116">L’exemple suivant montre **FindComputer** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1845d-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="1845d-117">Le résultat de ce code est le même que si vous appuyez sur le bouton **Démarrer** , sur **Rechercher**, sur l’option **imprimantes, ordinateurs ou personnes** , puis sur **un ordinateur sur le réseau**.</span><span class="sxs-lookup"><span data-stu-id="1845d-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="1845d-118">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1845d-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1845d-119">Langage</span><span class="sxs-lookup"><span data-stu-id="1845d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="1845d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="1845d-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1845d-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="1845d-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1845d-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1845d-122">Requirements</span></span>



| <span data-ttu-id="1845d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1845d-123">Requirement</span></span> | <span data-ttu-id="1845d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1845d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1845d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1845d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1845d-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1845d-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1845d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1845d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1845d-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1845d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1845d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1845d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1845d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1845d-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1845d-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="1845d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1845d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1845d-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1845d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1845d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1845d-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1845d-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




