---
description: 'Méthode Shell. BrowseForFolder : crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de renvoyer l’objet Folder du dossier sélectionné.'
title: Shell. BrowseForFolder, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 26677173cce2b72d1a0ba6bdc941cd2407908712
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841810"
---
# <a name="shellbrowseforfolder-method"></a><span data-ttu-id="61ec3-103">Shell. BrowseForFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="61ec3-103">Shell.BrowseForFolder method</span></span>

<span data-ttu-id="61ec3-104">Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet [**dossier**](folder.md) du dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="61ec3-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ec3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61ec3-105">Syntax</span></span>


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="61ec3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61ec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ec3-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61ec3-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ec3-108">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="61ec3-108">Type: **Integer**</span></span>

<span data-ttu-id="61ec3-109">Handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="61ec3-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="61ec3-110">Cette valeur peut être zéro.</span><span class="sxs-lookup"><span data-stu-id="61ec3-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="61ec3-111">*sTitle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61ec3-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ec3-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="61ec3-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="61ec3-113">Valeur de **chaîne** qui représente le titre affiché dans la boîte de dialogue **Parcourir** .</span><span class="sxs-lookup"><span data-stu-id="61ec3-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="61ec3-114">*iOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61ec3-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61ec3-115">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="61ec3-115">Type: **Integer**</span></span>

<span data-ttu-id="61ec3-116">Valeur **entière** qui contient les options de la méthode.</span><span class="sxs-lookup"><span data-stu-id="61ec3-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="61ec3-117">Il peut s’agir de zéro ou d’une combinaison des valeurs figurant dans le membre **ulFlags** de la structure [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="61ec3-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="61ec3-118">*vRootFolder* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61ec3-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61ec3-119">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="61ec3-119">Type: **Variant**</span></span>

<span data-ttu-id="61ec3-120">Dossier racine à utiliser dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="61ec3-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="61ec3-121">L’utilisateur ne peut pas parcourir plus haut dans l’arborescence que ce dossier.</span><span class="sxs-lookup"><span data-stu-id="61ec3-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="61ec3-122">Si cette valeur n’est pas spécifiée, le dossier racine utilisé dans la boîte de dialogue est le bureau.</span><span class="sxs-lookup"><span data-stu-id="61ec3-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="61ec3-123">Cette valeur peut être une chaîne qui spécifie le chemin d’accès du dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="61ec3-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="61ec3-124">Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript.</span><span class="sxs-lookup"><span data-stu-id="61ec3-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="61ec3-125">Dans ce cas, les valeurs numériques doivent être utilisées à leur place.</span><span class="sxs-lookup"><span data-stu-id="61ec3-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61ec3-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61ec3-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="61ec3-127">JScript</span><span class="sxs-lookup"><span data-stu-id="61ec3-127">JScript</span></span>

<span data-ttu-id="61ec3-128">Type : **dossier \* \***</span><span class="sxs-lookup"><span data-stu-id="61ec3-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="61ec3-129">Référence d’objet à l’objet [**dossier**](folder.md) du dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="61ec3-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="61ec3-130">VB</span><span class="sxs-lookup"><span data-stu-id="61ec3-130">VB</span></span>

<span data-ttu-id="61ec3-131">Type : **dossier \* \***</span><span class="sxs-lookup"><span data-stu-id="61ec3-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="61ec3-132">Référence d’objet à l’objet [**dossier**](folder.md) du dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="61ec3-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="61ec3-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="61ec3-133">Examples</span></span>

<span data-ttu-id="61ec3-134">L’exemple suivant utilise **BrowseForFolder** pour afficher une fenêtre de navigation intitulée « example » enracinée dans le dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="61ec3-134">The following example uses **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="61ec3-135">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="61ec3-135">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="61ec3-136">Langage</span><span class="sxs-lookup"><span data-stu-id="61ec3-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="61ec3-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="61ec3-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="61ec3-138">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="61ec3-138">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="61ec3-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="61ec3-139">Requirements</span></span>



| <span data-ttu-id="61ec3-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61ec3-140">Requirement</span></span> | <span data-ttu-id="61ec3-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="61ec3-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ec3-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61ec3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="61ec3-143">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61ec3-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="61ec3-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61ec3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="61ec3-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61ec3-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="61ec3-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="61ec3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="61ec3-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="61ec3-147"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="61ec3-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="61ec3-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61ec3-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61ec3-149"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="61ec3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="61ec3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61ec3-151"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="61ec3-151"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
