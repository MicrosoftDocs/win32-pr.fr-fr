---
description: Shell. ExplorerPolicy, méthode-obtient la valeur d’une stratégie Windows Internet Explorer spécifiée.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Shell. ExplorerPolicy, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 765e1dc46edbe5a27292c5d8ff940e29b269f8dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083697"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="6e070-103">Shell. ExplorerPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="6e070-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="6e070-104">Obtient la valeur pour une stratégie Windows Internet Explorer spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6e070-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e070-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e070-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="6e070-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e070-107">*bstrPolicyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e070-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e070-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6e070-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6e070-109">**Chaîne** qui spécifie le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6e070-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e070-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e070-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6e070-111">JScript</span><span class="sxs-lookup"><span data-stu-id="6e070-111">JScript</span></span>

<span data-ttu-id="6e070-112">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="6e070-112">Type: **Variant\***</span></span>

<span data-ttu-id="6e070-113">Valeur associée au nom de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e070-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="6e070-114">VB</span><span class="sxs-lookup"><span data-stu-id="6e070-114">VB</span></span>

<span data-ttu-id="6e070-115">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="6e070-115">Type: **Variant\***</span></span>

<span data-ttu-id="6e070-116">Valeur associée au nom de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e070-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e070-117">Notes </span><span class="sxs-lookup"><span data-stu-id="6e070-117">Remarks</span></span>

<span data-ttu-id="6e070-118">Les administrateurs réseau peuvent contrôler et gérer l’environnement informatique de leurs utilisateurs en définissant des stratégies.</span><span class="sxs-lookup"><span data-stu-id="6e070-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="6e070-119">Le nom de la valeur spécifiée doit se trouver dans la **\_ \_** \\  \\  \\  \\  \\  \\ sous-clé de l'**Explorateur** de stratégies CurrentVersion de l’utilisateur actuel de HKEY Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6e070-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="6e070-120">Si le nom de la valeur n’existe pas, la méthode retourne la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="6e070-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="6e070-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="6e070-121">Examples</span></span>

<span data-ttu-id="6e070-122">Les exemples suivants illustrent l’utilisation correcte de **ExplorerPolicy** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6e070-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6e070-123">Langage</span><span class="sxs-lookup"><span data-stu-id="6e070-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="6e070-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="6e070-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6e070-125">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="6e070-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6e070-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e070-126">Requirements</span></span>



| <span data-ttu-id="6e070-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e070-127">Requirement</span></span> | <span data-ttu-id="6e070-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e070-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e070-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e070-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6e070-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e070-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="6e070-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e070-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6e070-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e070-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6e070-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e070-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e070-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e070-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6e070-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="6e070-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e070-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e070-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6e070-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6e070-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e070-138"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="6e070-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
