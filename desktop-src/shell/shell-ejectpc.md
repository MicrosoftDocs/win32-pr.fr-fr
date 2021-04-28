---
description: 'Méthode Shell. EjectPC : éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu Démarrer et à sélectionner éjecter le PC, si votre ordinateur prend en charge cette commande.'
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Shell. EjectPC, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5ec08aaa82d2f752fa06537434adede86b9d5a3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104347"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="17f8f-104">Shell. EjectPC, méthode</span><span class="sxs-lookup"><span data-stu-id="17f8f-104">Shell.EjectPC method</span></span>

<span data-ttu-id="17f8f-105">Éjecte l’ordinateur de sa station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="17f8f-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="17f8f-106">Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **éjecter le PC**, si votre ordinateur prend en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="17f8f-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17f8f-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="17f8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17f8f-108">Parameters</span></span>

<span data-ttu-id="17f8f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="17f8f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17f8f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="17f8f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="17f8f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="17f8f-111">JScript</span></span>

<span data-ttu-id="17f8f-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="17f8f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="17f8f-113">VB</span><span class="sxs-lookup"><span data-stu-id="17f8f-113">VB</span></span>

<span data-ttu-id="17f8f-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="17f8f-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="17f8f-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="17f8f-115">Examples</span></span>

<span data-ttu-id="17f8f-116">L’exemple suivant montre **EjectPC** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="17f8f-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="17f8f-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="17f8f-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="17f8f-118">Langage</span><span class="sxs-lookup"><span data-stu-id="17f8f-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="17f8f-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="17f8f-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="17f8f-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="17f8f-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="17f8f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f8f-121">Requirements</span></span>



| <span data-ttu-id="17f8f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17f8f-122">Requirement</span></span> | <span data-ttu-id="17f8f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="17f8f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f8f-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f8f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17f8f-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17f8f-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="17f8f-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f8f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17f8f-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17f8f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="17f8f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f8f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="17f8f-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f8f-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="17f8f-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="17f8f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17f8f-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17f8f-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="17f8f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="17f8f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17f8f-133"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="17f8f-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




