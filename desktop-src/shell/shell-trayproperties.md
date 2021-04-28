---
description: 'Méthode Shell. TrayProperties : affiche la boîte de dialogue Propriétés de la barre des tâches et du menu Démarrer. Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez Propriétés.'
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Shell. TrayProperties, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e09f6833fbf07c99fdbce9c02b020bcbb5361408
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104097"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="cc6c5-104">Shell. TrayProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="cc6c5-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="cc6c5-105">Affiche la boîte de dialogue **Propriétés de la barre des tâches et du menu Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="cc6c5-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="cc6c5-106">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc6c5-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc6c5-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="cc6c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc6c5-108">Parameters</span></span>

<span data-ttu-id="cc6c5-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cc6c5-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="cc6c5-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="cc6c5-110">Examples</span></span>

<span data-ttu-id="cc6c5-111">L’exemple suivant montre **TrayProperties** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="cc6c5-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="cc6c5-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cc6c5-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cc6c5-113">Langage</span><span class="sxs-lookup"><span data-stu-id="cc6c5-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="cc6c5-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="cc6c5-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cc6c5-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="cc6c5-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cc6c5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc6c5-116">Requirements</span></span>



| <span data-ttu-id="cc6c5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc6c5-117">Requirement</span></span> | <span data-ttu-id="cc6c5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc6c5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6c5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc6c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6c5-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc6c5-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cc6c5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc6c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6c5-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc6c5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cc6c5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc6c5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc6c5-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c5-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cc6c5-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="cc6c5-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc6c5-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c5-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cc6c5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cc6c5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc6c5-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="cc6c5-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




