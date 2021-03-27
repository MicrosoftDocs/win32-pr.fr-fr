---
description: Obtient la valeur pour une stratégie Windows Internet Explorer spécifiée.
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
ms.openlocfilehash: 57247ad328c647cf9cdde32ac1a2951dd8e364ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863134"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="2fdfb-103">Méthode IShellDispatch4. ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="2fdfb-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="2fdfb-104">Obtient la valeur pour une stratégie Windows Internet Explorer spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdfb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fdfb-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="2fdfb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fdfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fdfb-107">*bstrPolicyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fdfb-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fdfb-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2fdfb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2fdfb-109">**Chaîne** qui spécifie le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fdfb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fdfb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2fdfb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="2fdfb-111">JScript</span></span>

<span data-ttu-id="2fdfb-112">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="2fdfb-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="2fdfb-113">Valeur associée au nom de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="2fdfb-114">VB</span><span class="sxs-lookup"><span data-stu-id="2fdfb-114">VB</span></span>

<span data-ttu-id="2fdfb-115">Type : _*variante \**_</span><span class="sxs-lookup"><span data-stu-id="2fdfb-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="2fdfb-116">Valeur associée au nom de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fdfb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2fdfb-117">Remarks</span></span>

<span data-ttu-id="2fdfb-118">Les administrateurs réseau peuvent contrôler et gérer l’environnement informatique de leurs utilisateurs en définissant des stratégies.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="2fdfb-119">Le nom de la valeur spécifiée doit se trouver dans la sous-clé de l *\_ \_ **\\** **\\** **\\** **\\** **\\** **\\** 'Explorateur de stratégies CurrentVersion \* de l’utilisateur de _ HKEY CURRENT USER Software*.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="2fdfb-120">Si le nom de la valeur n’existe pas, la méthode retourne la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="2fdfb-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="2fdfb-121">Examples</span></span>

<span data-ttu-id="2fdfb-122">Les exemples suivants illustrent l’utilisation correcte de **ExplorerPolicy** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2fdfb-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2fdfb-123">Langage</span><span class="sxs-lookup"><span data-stu-id="2fdfb-123">JScript:</span></span>


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



<span data-ttu-id="2fdfb-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="2fdfb-124">VBScript:</span></span>


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



<span data-ttu-id="2fdfb-125">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="2fdfb-125">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2fdfb-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2fdfb-126">Requirements</span></span>



| <span data-ttu-id="2fdfb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fdfb-127">Requirement</span></span> | <span data-ttu-id="2fdfb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fdfb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdfb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fdfb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2fdfb-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fdfb-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="2fdfb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fdfb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2fdfb-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fdfb-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2fdfb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fdfb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fdfb-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fdfb-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2fdfb-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="2fdfb-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fdfb-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fdfb-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2fdfb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2fdfb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fdfb-138"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2fdfb-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
