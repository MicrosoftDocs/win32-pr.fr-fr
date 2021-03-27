---
description: Ouvre le dossier spécifié.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: IShellDispatch. Open, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753085"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="1207a-103">IShellDispatch. Open, méthode</span><span class="sxs-lookup"><span data-stu-id="1207a-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="1207a-104">Ouvre le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1207a-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1207a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1207a-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="1207a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1207a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1207a-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1207a-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1207a-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="1207a-108">Type: **Variant**</span></span>

<span data-ttu-id="1207a-109">Chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="1207a-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="1207a-110">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="1207a-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="1207a-111">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="1207a-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="1207a-112">Si *vdir* est défini sur l’un des [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) et que le dossier spécial n’existe pas, cette fonction crée le dossier.</span><span class="sxs-lookup"><span data-stu-id="1207a-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1207a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1207a-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1207a-114">JScript</span><span class="sxs-lookup"><span data-stu-id="1207a-114">JScript</span></span>

<span data-ttu-id="1207a-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1207a-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1207a-116">VB</span><span class="sxs-lookup"><span data-stu-id="1207a-116">VB</span></span>

<span data-ttu-id="1207a-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1207a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1207a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1207a-118">Remarks</span></span>

<span data-ttu-id="1207a-119">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Open**](shell-open.md) .</span><span class="sxs-lookup"><span data-stu-id="1207a-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1207a-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="1207a-120">Examples</span></span>

<span data-ttu-id="1207a-121">Les exemples suivants illustrent l’utilisation de **Open** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1207a-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1207a-122">Langage</span><span class="sxs-lookup"><span data-stu-id="1207a-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="1207a-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="1207a-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1207a-124">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="1207a-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1207a-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1207a-125">Requirements</span></span>



| <span data-ttu-id="1207a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1207a-126">Requirement</span></span> | <span data-ttu-id="1207a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="1207a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1207a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1207a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1207a-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1207a-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1207a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1207a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1207a-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1207a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1207a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="1207a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1207a-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1207a-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1207a-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="1207a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1207a-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1207a-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1207a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1207a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1207a-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1207a-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1207a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1207a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1207a-139">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="1207a-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="1207a-140">**Explorer**</span><span class="sxs-lookup"><span data-stu-id="1207a-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




