---
description: Crée et retourne un objet Folder pour le dossier spécifié.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Méthode IShellDispatch. NameSpace (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527345"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="c1e0a-103">IShellDispatch. NameSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="c1e0a-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="c1e0a-104">Crée et retourne un objet [**Folder**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1e0a-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="c1e0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1e0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e0a-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1e0a-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e0a-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="c1e0a-108">Type: **Variant**</span></span>

<span data-ttu-id="c1e0a-109">Dossier pour lequel créer l’objet [**dossier**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="c1e0a-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="c1e0a-110">Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="c1e0a-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="c1e0a-111">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="c1e0a-112">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e0a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1e0a-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c1e0a-114">JScript</span><span class="sxs-lookup"><span data-stu-id="c1e0a-114">JScript</span></span>

<span data-ttu-id="c1e0a-115">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1e0a-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="c1e0a-116">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="c1e0a-117">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="c1e0a-118">VB</span><span class="sxs-lookup"><span data-stu-id="c1e0a-118">VB</span></span>

<span data-ttu-id="c1e0a-119">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1e0a-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="c1e0a-120">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="c1e0a-121">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e0a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="c1e0a-122">Remarks</span></span>

<span data-ttu-id="c1e0a-123">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Namespace**](shell-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="c1e0a-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c1e0a-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="c1e0a-124">Examples</span></span>

<span data-ttu-id="c1e0a-125">Les exemples suivants illustrent l’utilisation de l' [**espace de noms**](shell-namespace.md) dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1e0a-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c1e0a-126">Langage</span><span class="sxs-lookup"><span data-stu-id="c1e0a-126">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="c1e0a-127">VBScript</span><span class="sxs-lookup"><span data-stu-id="c1e0a-127">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c1e0a-128">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="c1e0a-128">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c1e0a-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c1e0a-129">Requirements</span></span>



| <span data-ttu-id="c1e0a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1e0a-130">Requirement</span></span> | <span data-ttu-id="c1e0a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e0a-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e0a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1e0a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e0a-133">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1e0a-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1e0a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1e0a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e0a-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1e0a-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c1e0a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1e0a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e0a-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e0a-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c1e0a-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="c1e0a-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1e0a-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1e0a-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c1e0a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c1e0a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1e0a-141"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e0a-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




