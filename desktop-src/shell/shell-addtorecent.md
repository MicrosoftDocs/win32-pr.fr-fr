---
description: Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).
ms.assetid: 26D2AE5A-FC7E-4c7c-9F10-8D3D7AA236E7
title: Shell. AddToRecent, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c4372cc6cfac25f94e607f14734a9f544cd4fcbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973775"
---
# <a name="shelladdtorecent-method"></a><span data-ttu-id="9f65b-103">Shell. AddToRecent, méthode</span><span class="sxs-lookup"><span data-stu-id="9f65b-103">Shell.AddToRecent method</span></span>

<span data-ttu-id="9f65b-104">Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="9f65b-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f65b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f65b-105">Syntax</span></span>


```JScript
Shell.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

Shell.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a><span data-ttu-id="9f65b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f65b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f65b-107">*varFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f65b-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f65b-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="9f65b-108">Type: **Variant**</span></span>

<span data-ttu-id="9f65b-109">**Chaîne** qui contient le chemin d’accès du fichier à ajouter à la liste des documents récemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="9f65b-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="9f65b-110">**Windows Vista**: définissez ce paramètre sur la **valeur null** pour effacer le dossier documents récents.</span><span class="sxs-lookup"><span data-stu-id="9f65b-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="9f65b-111">*bstrCategory* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9f65b-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f65b-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9f65b-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9f65b-113">**Chaîne** qui contient le nom de la catégorie dans laquelle placer le fichier.</span><span class="sxs-lookup"><span data-stu-id="9f65b-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f65b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f65b-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9f65b-115">JScript</span><span class="sxs-lookup"><span data-stu-id="9f65b-115">JScript</span></span>

<span data-ttu-id="9f65b-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f65b-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9f65b-117">VB</span><span class="sxs-lookup"><span data-stu-id="9f65b-117">VB</span></span>

<span data-ttu-id="9f65b-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f65b-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="9f65b-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="9f65b-119">Examples</span></span>

<span data-ttu-id="9f65b-120">Les exemples suivants illustrent l’utilisation de **AddToRecent** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9f65b-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9f65b-121">Langage</span><span class="sxs-lookup"><span data-stu-id="9f65b-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



<span data-ttu-id="9f65b-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="9f65b-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9f65b-123">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="9f65b-123">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9f65b-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f65b-124">Requirements</span></span>



| <span data-ttu-id="9f65b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f65b-125">Requirement</span></span> | <span data-ttu-id="9f65b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f65b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f65b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f65b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9f65b-128">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f65b-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9f65b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f65b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9f65b-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f65b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f65b-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f65b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f65b-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f65b-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9f65b-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="9f65b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f65b-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f65b-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9f65b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9f65b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f65b-136"><dt>Shell32.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9f65b-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
