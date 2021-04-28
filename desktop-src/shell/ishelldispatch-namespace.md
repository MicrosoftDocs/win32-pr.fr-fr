---
description: 'Méthode IShellDispatch. NameSpace : crée et retourne un objet Folder pour le dossier spécifié.'
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
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100517"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="d46e0-103">IShellDispatch. NameSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="d46e0-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="d46e0-104">Crée et retourne un objet [**Folder**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d46e0-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="d46e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d46e0-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="d46e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d46e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d46e0-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d46e0-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d46e0-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="d46e0-108">Type: **Variant**</span></span>

<span data-ttu-id="d46e0-109">Dossier pour lequel créer l’objet [**dossier**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="d46e0-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="d46e0-110">Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="d46e0-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="d46e0-111">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="d46e0-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="d46e0-112">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="d46e0-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d46e0-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d46e0-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d46e0-114">JScript</span><span class="sxs-lookup"><span data-stu-id="d46e0-114">JScript</span></span>

<span data-ttu-id="d46e0-115">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d46e0-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="d46e0-116">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d46e0-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="d46e0-117">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="d46e0-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="d46e0-118">VB</span><span class="sxs-lookup"><span data-stu-id="d46e0-118">VB</span></span>

<span data-ttu-id="d46e0-119">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d46e0-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="d46e0-120">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d46e0-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="d46e0-121">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="d46e0-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d46e0-122">Notes </span><span class="sxs-lookup"><span data-stu-id="d46e0-122">Remarks</span></span>

<span data-ttu-id="d46e0-123">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Namespace**](shell-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="d46e0-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="d46e0-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="d46e0-124">Examples</span></span>

<span data-ttu-id="d46e0-125">Les exemples suivants illustrent l’utilisation de l' [**espace de noms**](shell-namespace.md) dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d46e0-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d46e0-126">Langage</span><span class="sxs-lookup"><span data-stu-id="d46e0-126">JScript:</span></span>


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



<span data-ttu-id="d46e0-127">VBScript</span><span class="sxs-lookup"><span data-stu-id="d46e0-127">VBScript:</span></span>


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



<span data-ttu-id="d46e0-128">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="d46e0-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d46e0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d46e0-129">Requirements</span></span>



| <span data-ttu-id="d46e0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d46e0-130">Requirement</span></span> | <span data-ttu-id="d46e0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d46e0-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46e0-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46e0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d46e0-133">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d46e0-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d46e0-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d46e0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d46e0-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d46e0-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d46e0-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d46e0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46e0-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d46e0-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d46e0-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="d46e0-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d46e0-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d46e0-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d46e0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d46e0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d46e0-141"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d46e0-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




