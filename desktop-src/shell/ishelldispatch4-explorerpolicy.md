---
description: 'Méthode IShellDispatch4. ExplorerPolicy : obtient la valeur d’une stratégie Windows Internet Explorer spécifiée.'
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Méthode IShellDispatch4. ExplorerPolicy (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116827"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="f0bb1-103">Méthode IShellDispatch4. ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="f0bb1-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="f0bb1-104">Obtient la valeur pour une stratégie Windows Internet Explorer spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0bb1-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="f0bb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0bb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0bb1-107">*bstrPolicyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0bb1-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0bb1-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f0bb1-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f0bb1-109">**Chaîne** qui spécifie le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0bb1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0bb1-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f0bb1-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f0bb1-111">JScript</span></span>

<span data-ttu-id="f0bb1-112">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="f0bb1-112">Type: **Variant\***</span></span>

<span data-ttu-id="f0bb1-113">Valeur associée au nom de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="f0bb1-114">VB</span><span class="sxs-lookup"><span data-stu-id="f0bb1-114">VB</span></span>

<span data-ttu-id="f0bb1-115">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="f0bb1-115">Type: **Variant\***</span></span>

<span data-ttu-id="f0bb1-116">Valeur associée au nom de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0bb1-117">Notes </span><span class="sxs-lookup"><span data-stu-id="f0bb1-117">Remarks</span></span>

<span data-ttu-id="f0bb1-118">Les administrateurs réseau peuvent contrôler et gérer l’environnement informatique de leurs utilisateurs en définissant des stratégies.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="f0bb1-119">Le nom de la valeur spécifiée doit se trouver dans la **\_ \_** \\  \\  \\  \\  \\  \\ sous-clé de l'**Explorateur** de stratégies CurrentVersion de l’utilisateur actuel de HKEY Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="f0bb1-120">Si le nom de la valeur n’existe pas, la méthode retourne la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="f0bb1-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="f0bb1-121">Examples</span></span>

<span data-ttu-id="f0bb1-122">Les exemples suivants illustrent l’utilisation correcte de **ExplorerPolicy** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f0bb1-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f0bb1-123">Langage</span><span class="sxs-lookup"><span data-stu-id="f0bb1-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="f0bb1-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="f0bb1-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f0bb1-125">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="f0bb1-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f0bb1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0bb1-126">Requirements</span></span>



| <span data-ttu-id="f0bb1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0bb1-127">Requirement</span></span> | <span data-ttu-id="f0bb1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0bb1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0bb1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0bb1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0bb1-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0bb1-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="f0bb1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0bb1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0bb1-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0bb1-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0bb1-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0bb1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0bb1-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0bb1-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f0bb1-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="f0bb1-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0bb1-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0bb1-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f0bb1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f0bb1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0bb1-138"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="f0bb1-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
