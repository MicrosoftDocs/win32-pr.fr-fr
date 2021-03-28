---
description: Ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: IShellDispatch. explore, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1ae29b4962dcac1be0b7ea23808e36ce005cb62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972430"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="41d27-103">IShellDispatch. explore, méthode</span><span class="sxs-lookup"><span data-stu-id="41d27-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="41d27-104">Ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="41d27-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41d27-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="41d27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41d27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d27-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41d27-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d27-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="41d27-108">Type: **Variant**</span></span>

<span data-ttu-id="41d27-109">Dossier à afficher.</span><span class="sxs-lookup"><span data-stu-id="41d27-109">The folder to be displayed.</span></span> <span data-ttu-id="41d27-110">Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="41d27-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="41d27-111">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="41d27-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="41d27-112">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="41d27-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d27-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41d27-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="41d27-114">JScript</span><span class="sxs-lookup"><span data-stu-id="41d27-114">JScript</span></span>

<span data-ttu-id="41d27-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="41d27-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="41d27-116">VB</span><span class="sxs-lookup"><span data-stu-id="41d27-116">VB</span></span>

<span data-ttu-id="41d27-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="41d27-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d27-118">Notes</span><span class="sxs-lookup"><span data-stu-id="41d27-118">Remarks</span></span>

<span data-ttu-id="41d27-119">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. explore**](shell-explore.md) .</span><span class="sxs-lookup"><span data-stu-id="41d27-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="41d27-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="41d27-120">Examples</span></span>

<span data-ttu-id="41d27-121">Les exemples suivants illustrent l’utilisation de l' **exploration** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="41d27-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="41d27-122">Langage</span><span class="sxs-lookup"><span data-stu-id="41d27-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="41d27-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="41d27-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="41d27-124">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="41d27-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="41d27-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41d27-125">Requirements</span></span>



| <span data-ttu-id="41d27-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41d27-126">Requirement</span></span> | <span data-ttu-id="41d27-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="41d27-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d27-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d27-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41d27-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41d27-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="41d27-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d27-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41d27-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41d27-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41d27-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="41d27-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="41d27-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d27-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="41d27-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="41d27-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41d27-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41d27-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="41d27-136">DLL</span><span class="sxs-lookup"><span data-stu-id="41d27-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d27-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="41d27-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




