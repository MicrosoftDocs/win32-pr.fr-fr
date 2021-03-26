---
description: Affiche la boîte de dialogue Propriétés de la barre des tâches et du menu Démarrer. Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez Propriétés.
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
ms.openlocfilehash: da3fbfdb2b6aa2517b275041856920c6b2cd1bb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973674"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="f1702-104">Shell. TrayProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="f1702-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="f1702-105">Affiche la boîte de dialogue **Propriétés de la barre des tâches et du menu Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="f1702-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="f1702-106">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f1702-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1702-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1702-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="f1702-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1702-108">Parameters</span></span>

<span data-ttu-id="f1702-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f1702-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="f1702-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="f1702-110">Examples</span></span>

<span data-ttu-id="f1702-111">L’exemple suivant montre **TrayProperties** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f1702-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="f1702-112">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f1702-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f1702-113">Langage</span><span class="sxs-lookup"><span data-stu-id="f1702-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="f1702-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="f1702-114">VBScript:</span></span>


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



<span data-ttu-id="f1702-115">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="f1702-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f1702-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f1702-116">Requirements</span></span>



| <span data-ttu-id="f1702-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1702-117">Requirement</span></span> | <span data-ttu-id="f1702-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1702-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1702-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1702-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1702-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1702-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f1702-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1702-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1702-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1702-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1702-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1702-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1702-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1702-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f1702-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="f1702-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1702-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1702-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f1702-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f1702-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1702-128"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="f1702-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




