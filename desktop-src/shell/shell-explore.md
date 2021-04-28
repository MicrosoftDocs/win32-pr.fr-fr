---
description: 'Méthode Shell. explore : ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.'
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Shell. explore, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104327"
---
# <a name="shellexplore-method"></a><span data-ttu-id="10e26-103">Shell. explore (méthode)</span><span class="sxs-lookup"><span data-stu-id="10e26-103">Shell.Explore method</span></span>

<span data-ttu-id="10e26-104">Ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="10e26-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10e26-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="10e26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10e26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e26-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10e26-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e26-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="10e26-108">Type: **Variant**</span></span>

<span data-ttu-id="10e26-109">Dossier à afficher.</span><span class="sxs-lookup"><span data-stu-id="10e26-109">The folder to be displayed.</span></span> <span data-ttu-id="10e26-110">Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="10e26-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="10e26-111">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="10e26-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="10e26-112">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="10e26-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e26-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="10e26-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="10e26-114">JScript</span><span class="sxs-lookup"><span data-stu-id="10e26-114">JScript</span></span>

<span data-ttu-id="10e26-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="10e26-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="10e26-116">VB</span><span class="sxs-lookup"><span data-stu-id="10e26-116">VB</span></span>

<span data-ttu-id="10e26-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="10e26-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="10e26-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="10e26-118">Examples</span></span>

<span data-ttu-id="10e26-119">L’exemple suivant montre l' **exploration** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="10e26-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="10e26-120">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10e26-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="10e26-121">Langage</span><span class="sxs-lookup"><span data-stu-id="10e26-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="10e26-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="10e26-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="10e26-123">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="10e26-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="10e26-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10e26-124">Requirements</span></span>



| <span data-ttu-id="10e26-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10e26-125">Requirement</span></span> | <span data-ttu-id="10e26-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="10e26-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e26-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10e26-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10e26-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10e26-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="10e26-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10e26-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10e26-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10e26-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10e26-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="10e26-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e26-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10e26-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="10e26-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="10e26-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10e26-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10e26-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="10e26-135">DLL</span><span class="sxs-lookup"><span data-stu-id="10e26-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10e26-136"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="10e26-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




