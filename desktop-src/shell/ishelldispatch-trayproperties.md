---
description: Affiche la boîte de dialogue Propriétés de la barre des tâches et du menu Démarrer. Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez Propriétés.
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Méthode IShellDispatch. TrayProperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5e22dd48b77035aab3754a4c8e3d2c414ec606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951376"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="ac886-104">Méthode IShellDispatch. TrayProperties</span><span class="sxs-lookup"><span data-stu-id="ac886-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="ac886-105">Affiche la boîte de dialogue **Propriétés de la barre des tâches et du menu Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="ac886-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="ac886-106">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ac886-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac886-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac886-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="ac886-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac886-108">Parameters</span></span>

<span data-ttu-id="ac886-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ac886-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac886-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac886-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ac886-111">JScript</span><span class="sxs-lookup"><span data-stu-id="ac886-111">JScript</span></span>

<span data-ttu-id="ac886-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ac886-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ac886-113">VB</span><span class="sxs-lookup"><span data-stu-id="ac886-113">VB</span></span>

<span data-ttu-id="ac886-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ac886-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac886-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ac886-115">Remarks</span></span>

<span data-ttu-id="ac886-116">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. TrayProperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="ac886-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="ac886-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="ac886-117">Examples</span></span>

<span data-ttu-id="ac886-118">Les exemples suivants illustrent l’utilisation de **TrayProperties** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac886-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ac886-119">Langage</span><span class="sxs-lookup"><span data-stu-id="ac886-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="ac886-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="ac886-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ac886-121">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="ac886-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ac886-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ac886-122">Requirements</span></span>



| <span data-ttu-id="ac886-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac886-123">Requirement</span></span> | <span data-ttu-id="ac886-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac886-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac886-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac886-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ac886-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac886-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac886-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac886-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ac886-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac886-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ac886-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac886-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac886-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac886-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ac886-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="ac886-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac886-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac886-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ac886-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ac886-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac886-134"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ac886-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




