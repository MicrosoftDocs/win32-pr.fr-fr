---
description: En savoir plus sur la méthode IShellDispatch. RefreshMenu, qui actualise le contenu du menu Démarrer. Utilisé uniquement avec les systèmes antérieurs à Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Méthode IShellDispatch. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404672"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="99aea-104">Méthode IShellDispatch. RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="99aea-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="99aea-105">Actualise le contenu du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="99aea-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="99aea-106">Utilisé uniquement avec les systèmes antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="99aea-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="99aea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99aea-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="99aea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99aea-108">Parameters</span></span>

<span data-ttu-id="99aea-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="99aea-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99aea-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99aea-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="99aea-111">JScript</span><span class="sxs-lookup"><span data-stu-id="99aea-111">JScript</span></span>

<span data-ttu-id="99aea-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="99aea-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="99aea-113">VB</span><span class="sxs-lookup"><span data-stu-id="99aea-113">VB</span></span>

<span data-ttu-id="99aea-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="99aea-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99aea-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="99aea-115">Remarks</span></span>

<span data-ttu-id="99aea-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. TrayProperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="99aea-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="99aea-117">La fonctionnalité fournie par **RefreshMenu** est gérée automatiquement sous Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="99aea-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="99aea-118">N’appelez pas cette méthode sur Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="99aea-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="99aea-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="99aea-119">Examples</span></span>

<span data-ttu-id="99aea-120">Les exemples suivants illustrent l’utilisation de **RefreshMenu** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="99aea-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="99aea-121">Langage</span><span class="sxs-lookup"><span data-stu-id="99aea-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="99aea-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="99aea-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="99aea-123">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="99aea-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="99aea-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="99aea-124">Requirements</span></span>



| <span data-ttu-id="99aea-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99aea-125">Requirement</span></span> | <span data-ttu-id="99aea-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="99aea-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99aea-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99aea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99aea-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99aea-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="99aea-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99aea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99aea-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99aea-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99aea-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="99aea-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="99aea-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99aea-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="99aea-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="99aea-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99aea-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="99aea-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="99aea-135">DLL</span><span class="sxs-lookup"><span data-stu-id="99aea-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99aea-136"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="99aea-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




