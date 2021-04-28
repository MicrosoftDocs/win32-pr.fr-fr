---
description: 'Shell. NameSpace, méthode : crée et retourne un objet Folder pour le dossier spécifié.'
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
ms.openlocfilehash: fab501912c55aaaf6cab832bf76763672e830d33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083707"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="416d7-103">Shell. NameSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="416d7-103">Shell.NameSpace method</span></span>

<span data-ttu-id="416d7-104">Crée et retourne un objet [**Folder**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="416d7-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="416d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="416d7-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="416d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="416d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="416d7-107">*vdir* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="416d7-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416d7-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="416d7-108">Type: **Variant**</span></span>

<span data-ttu-id="416d7-109">Dossier pour lequel créer l’objet [**dossier**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="416d7-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="416d7-110">Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="416d7-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="416d7-111">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="416d7-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="416d7-112">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="416d7-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="416d7-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="416d7-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="416d7-114">JScript</span><span class="sxs-lookup"><span data-stu-id="416d7-114">JScript</span></span>

<span data-ttu-id="416d7-115">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="416d7-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="416d7-116">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="416d7-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="416d7-117">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="416d7-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="416d7-118">VB</span><span class="sxs-lookup"><span data-stu-id="416d7-118">VB</span></span>

<span data-ttu-id="416d7-119">Type : **[ **dossier**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="416d7-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="416d7-120">Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="416d7-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="416d7-121">Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="416d7-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="416d7-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="416d7-122">Examples</span></span>

<span data-ttu-id="416d7-123">L’exemple suivant illustre l’utilisation de l' **espace de noms** .</span><span class="sxs-lookup"><span data-stu-id="416d7-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="416d7-124">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="416d7-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="416d7-125">Langage</span><span class="sxs-lookup"><span data-stu-id="416d7-125">JScript:</span></span>


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



<span data-ttu-id="416d7-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="416d7-126">VBScript:</span></span>


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



<span data-ttu-id="416d7-127">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="416d7-127">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="416d7-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="416d7-128">Requirements</span></span>



| <span data-ttu-id="416d7-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="416d7-129">Requirement</span></span> | <span data-ttu-id="416d7-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="416d7-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416d7-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="416d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="416d7-132">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="416d7-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="416d7-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="416d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="416d7-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="416d7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="416d7-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="416d7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="416d7-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="416d7-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="416d7-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="416d7-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="416d7-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="416d7-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="416d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="416d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416d7-140"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="416d7-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




