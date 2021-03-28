---
description: Exécute l’application du panneau de configuration spécifiée.
title: Méthode IShellDispatch. ControlPanelItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527352"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="77319-103">Méthode IShellDispatch. ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="77319-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="77319-104">Exécute l’application du panneau de configuration spécifiée.</span><span class="sxs-lookup"><span data-stu-id="77319-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="77319-105">Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="77319-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="77319-106">À compter de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="77319-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="77319-107">Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe.</span><span class="sxs-lookup"><span data-stu-id="77319-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="77319-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="77319-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="77319-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77319-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="77319-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77319-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77319-111">*bstrDir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77319-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77319-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="77319-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="77319-113">Nom de fichier de l’application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="77319-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77319-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77319-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="77319-115">JScript</span><span class="sxs-lookup"><span data-stu-id="77319-115">JScript</span></span>

<span data-ttu-id="77319-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="77319-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="77319-117">VB</span><span class="sxs-lookup"><span data-stu-id="77319-117">VB</span></span>

<span data-ttu-id="77319-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="77319-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77319-119">Notes</span><span class="sxs-lookup"><span data-stu-id="77319-119">Remarks</span></span>

<span data-ttu-id="77319-120">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ControlPanelItem**](shell-controlpanelitem.md) .</span><span class="sxs-lookup"><span data-stu-id="77319-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="77319-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="77319-121">Examples</span></span>

<span data-ttu-id="77319-122">Les exemples suivants utilisent [**ControlPanelItem**](shell-controlpanelitem.md) pour exécuter l’élément des **propriétés d’affichage** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="77319-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="77319-123">L’utilisation est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="77319-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="77319-124">Langage</span><span class="sxs-lookup"><span data-stu-id="77319-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="77319-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="77319-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="77319-126">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="77319-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="77319-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77319-127">Requirements</span></span>



| <span data-ttu-id="77319-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77319-128">Requirement</span></span> | <span data-ttu-id="77319-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="77319-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77319-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77319-130">Minimum supported client</span></span><br/> | <span data-ttu-id="77319-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77319-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="77319-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77319-132">Minimum supported server</span></span><br/> | <span data-ttu-id="77319-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77319-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="77319-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="77319-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="77319-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77319-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="77319-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="77319-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77319-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77319-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="77319-138">DLL</span><span class="sxs-lookup"><span data-stu-id="77319-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77319-139"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="77319-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
