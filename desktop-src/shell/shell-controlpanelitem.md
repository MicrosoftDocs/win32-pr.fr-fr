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
ms.openlocfilehash: dec27dab8bd37cc9c15e603c24a54d528cea331a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973330"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="d6aed-103">Shell. ControlPanelItem, méthode</span><span class="sxs-lookup"><span data-stu-id="d6aed-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="d6aed-104">Exécute l’application spécifiée du panneau de configuration ( \* . cpl).</span><span class="sxs-lookup"><span data-stu-id="d6aed-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="d6aed-105">Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6aed-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="d6aed-106">À compter de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d6aed-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="d6aed-107">Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe.</span><span class="sxs-lookup"><span data-stu-id="d6aed-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="d6aed-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d6aed-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="d6aed-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6aed-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="d6aed-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6aed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6aed-111">*bstrDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6aed-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6aed-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d6aed-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d6aed-113">Nom de fichier de l’application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d6aed-113">The Control Panel application's file name.</span></span> <span data-ttu-id="d6aed-114">Toutes les applications du panneau de configuration ont l’extension. cpl.</span><span class="sxs-lookup"><span data-stu-id="d6aed-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6aed-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6aed-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d6aed-116">JScript</span><span class="sxs-lookup"><span data-stu-id="d6aed-116">JScript</span></span>

<span data-ttu-id="d6aed-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d6aed-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d6aed-118">VB</span><span class="sxs-lookup"><span data-stu-id="d6aed-118">VB</span></span>

<span data-ttu-id="d6aed-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d6aed-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d6aed-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="d6aed-120">Examples</span></span>

<span data-ttu-id="d6aed-121">L’exemple suivant utilise **ControlPanelItem** pour exécuter l’élément des **propriétés d’affichage** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d6aed-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="d6aed-122">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d6aed-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d6aed-123">Langage</span><span class="sxs-lookup"><span data-stu-id="d6aed-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="d6aed-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="d6aed-124">VBScript:</span></span>


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



<span data-ttu-id="d6aed-125">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="d6aed-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d6aed-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6aed-126">Requirements</span></span>



| <span data-ttu-id="d6aed-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6aed-127">Requirement</span></span> | <span data-ttu-id="d6aed-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6aed-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6aed-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6aed-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d6aed-130">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6aed-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d6aed-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6aed-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d6aed-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6aed-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6aed-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6aed-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6aed-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6aed-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d6aed-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="d6aed-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6aed-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6aed-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d6aed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d6aed-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6aed-138"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d6aed-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
