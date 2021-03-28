---
description: Ouvre le dossier spécifié.
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Shell. Open, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3572f48a7b129500c38c3c0227ba479ecb775067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866145"
---
# <a name="shellopen-method"></a><span data-ttu-id="7ed88-103">Shell. Open, méthode</span><span class="sxs-lookup"><span data-stu-id="7ed88-103">Shell.Open method</span></span>

<span data-ttu-id="7ed88-104">Ouvre le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ed88-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed88-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ed88-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="7ed88-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ed88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ed88-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ed88-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ed88-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="7ed88-108">Type: **Variant**</span></span>

<span data-ttu-id="7ed88-109">Chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="7ed88-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="7ed88-110">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="7ed88-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="7ed88-111">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="7ed88-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="7ed88-112">Si *vdir* est défini sur l’un des [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) et que le dossier spécial n’existe pas, cette fonction crée le dossier.</span><span class="sxs-lookup"><span data-stu-id="7ed88-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7ed88-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="7ed88-113">Examples</span></span>

<span data-ttu-id="7ed88-114">L’exemple suivant montre l' **ouverture** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7ed88-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="7ed88-115">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7ed88-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7ed88-116">Langage</span><span class="sxs-lookup"><span data-stu-id="7ed88-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="7ed88-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="7ed88-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7ed88-118">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7ed88-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7ed88-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ed88-119">Requirements</span></span>



| <span data-ttu-id="7ed88-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ed88-120">Requirement</span></span> | <span data-ttu-id="7ed88-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ed88-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed88-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed88-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed88-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ed88-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ed88-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ed88-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed88-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ed88-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ed88-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ed88-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed88-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed88-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7ed88-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="7ed88-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ed88-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ed88-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7ed88-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7ed88-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ed88-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="7ed88-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ed88-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ed88-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed88-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="7ed88-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="7ed88-134">**Explorer**</span><span class="sxs-lookup"><span data-stu-id="7ed88-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




