---
description: Crée un nouveau dossier.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Folder. NewFolder, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951947"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="be203-103">Folder. NewFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="be203-103">Folder.NewFolder method</span></span>

<span data-ttu-id="be203-104">Crée un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="be203-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="be203-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be203-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="be203-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be203-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be203-107">*bName*</span><span class="sxs-lookup"><span data-stu-id="be203-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="be203-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="be203-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="be203-109">Chaîne qui spécifie le nom du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="be203-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="be203-110">*vOptions* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="be203-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be203-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="be203-111">Type: **Variant**</span></span>

<span data-ttu-id="be203-112">Cette valeur n’est pas utilisée actuellement.</span><span class="sxs-lookup"><span data-stu-id="be203-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be203-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be203-113">Return value</span></span>

<span data-ttu-id="be203-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be203-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be203-115">Notes</span><span class="sxs-lookup"><span data-stu-id="be203-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be203-116">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="be203-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="be203-117">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="be203-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="be203-118">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="be203-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="be203-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="be203-119">Examples</span></span>

<span data-ttu-id="be203-120">L’exemple suivant utilise **NewFolder** pour créer le nouveau dossier C : \\ TestFolder.</span><span class="sxs-lookup"><span data-stu-id="be203-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="be203-121">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="be203-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="be203-122">Langage</span><span class="sxs-lookup"><span data-stu-id="be203-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="be203-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="be203-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="be203-124">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="be203-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="be203-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="be203-125">Requirements</span></span>



| <span data-ttu-id="be203-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be203-126">Requirement</span></span> | <span data-ttu-id="be203-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="be203-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be203-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be203-128">Minimum supported client</span></span><br/> | <span data-ttu-id="be203-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be203-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="be203-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be203-130">Minimum supported server</span></span><br/> | <span data-ttu-id="be203-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be203-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be203-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="be203-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="be203-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be203-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="be203-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="be203-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be203-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be203-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="be203-136">DLL</span><span class="sxs-lookup"><span data-stu-id="be203-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be203-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="be203-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
