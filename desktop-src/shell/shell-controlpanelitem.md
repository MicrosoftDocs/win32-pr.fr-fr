---
description: Exécute l’application spécifiée du panneau de configuration ( \* . cpl).
title: Shell. ControlPanelItem, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841800"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="83833-103">Shell. ControlPanelItem, méthode</span><span class="sxs-lookup"><span data-stu-id="83833-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="83833-104">Exécute l’application spécifiée du panneau de configuration ( \* . cpl).</span><span class="sxs-lookup"><span data-stu-id="83833-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="83833-105">Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="83833-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="83833-106">À compter de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="83833-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="83833-107">Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe.</span><span class="sxs-lookup"><span data-stu-id="83833-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="83833-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="83833-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="83833-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83833-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="83833-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83833-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83833-111">*bstrDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83833-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83833-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="83833-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="83833-113">Nom de fichier de l’application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="83833-113">The Control Panel application's file name.</span></span> <span data-ttu-id="83833-114">Toutes les applications du panneau de configuration ont l’extension. cpl.</span><span class="sxs-lookup"><span data-stu-id="83833-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83833-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="83833-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="83833-116">JScript</span><span class="sxs-lookup"><span data-stu-id="83833-116">JScript</span></span>

<span data-ttu-id="83833-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="83833-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="83833-118">VB</span><span class="sxs-lookup"><span data-stu-id="83833-118">VB</span></span>

<span data-ttu-id="83833-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="83833-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="83833-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="83833-120">Examples</span></span>

<span data-ttu-id="83833-121">L’exemple suivant utilise **ControlPanelItem** pour exécuter l’élément des **propriétés d’affichage** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="83833-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="83833-122">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="83833-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="83833-123">Langage</span><span class="sxs-lookup"><span data-stu-id="83833-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="83833-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="83833-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="83833-125">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="83833-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="83833-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83833-126">Requirements</span></span>



| <span data-ttu-id="83833-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83833-127">Requirement</span></span> | <span data-ttu-id="83833-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="83833-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83833-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83833-129">Minimum supported client</span></span><br/> | <span data-ttu-id="83833-130">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83833-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="83833-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83833-131">Minimum supported server</span></span><br/> | <span data-ttu-id="83833-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83833-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83833-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="83833-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="83833-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="83833-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="83833-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="83833-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83833-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83833-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="83833-137">DLL</span><span class="sxs-lookup"><span data-stu-id="83833-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83833-138"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="83833-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
