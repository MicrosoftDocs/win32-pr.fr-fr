---
description: Crée et retourne un objet Folder pour le dossier spécifié.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Shell. NameSpace, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202903"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="82913-103">Shell. NameSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="82913-103">Shell.NameSpace method</span></span>

<span data-ttu-id="82913-104">Crée et retourne un objet [**Folder**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="82913-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="82913-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82913-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="82913-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82913-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82913-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82913-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82913-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="82913-108">Type: **Variant**</span></span>

<span data-ttu-id="82913-109">Dossier pour lequel créer l’objet [**dossier**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="82913-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="82913-110">Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="82913-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="82913-111">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="82913-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="82913-112">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="82913-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82913-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82913-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="82913-114">JScript</span><span class="sxs-lookup"><span data-stu-id="82913-114">JScript</span></span>

<span data-ttu-id="82913-115">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="82913-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="82913-116">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="82913-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="82913-117">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="82913-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="82913-118">VB</span><span class="sxs-lookup"><span data-stu-id="82913-118">VB</span></span>

<span data-ttu-id="82913-119">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="82913-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="82913-120">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="82913-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="82913-121">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="82913-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="82913-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="82913-122">Examples</span></span>

<span data-ttu-id="82913-123">L’exemple suivant illustre l’utilisation de l' **espace de noms** .</span><span class="sxs-lookup"><span data-stu-id="82913-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="82913-124">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="82913-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="82913-125">Langage</span><span class="sxs-lookup"><span data-stu-id="82913-125">JScript:</span></span>


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



<span data-ttu-id="82913-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="82913-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="82913-127">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="82913-127">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="82913-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="82913-128">Requirements</span></span>



| <span data-ttu-id="82913-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82913-129">Requirement</span></span> | <span data-ttu-id="82913-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="82913-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82913-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82913-131">Minimum supported client</span></span><br/> | <span data-ttu-id="82913-132">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82913-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="82913-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82913-133">Minimum supported server</span></span><br/> | <span data-ttu-id="82913-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82913-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="82913-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="82913-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="82913-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="82913-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="82913-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="82913-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82913-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82913-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="82913-139">DLL</span><span class="sxs-lookup"><span data-stu-id="82913-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82913-140"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="82913-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




