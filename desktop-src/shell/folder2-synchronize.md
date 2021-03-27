---
description: Synchronise tous les fichiers hors connexion dans le dossier.
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Dossier2. Synchronize, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e9c39c37ff0e44e58aa71c69496dec8bee2745bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393251"
---
# <a name="folder2synchronize-method"></a><span data-ttu-id="2d2fc-103">Dossier2. Synchronize, méthode</span><span class="sxs-lookup"><span data-stu-id="2d2fc-103">Folder2.Synchronize method</span></span>

<span data-ttu-id="2d2fc-104">Synchronise tous les fichiers hors connexion dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-104">Synchronizes all offline files in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d2fc-105">Syntax</span></span>


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a><span data-ttu-id="2d2fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d2fc-106">Parameters</span></span>

<span data-ttu-id="2d2fc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d2fc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2d2fc-108">Remarks</span></span>

<span data-ttu-id="2d2fc-109">Pour utiliser cette méthode, vous devez activer la fonctionnalité Fichiers hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-109">To use this method, the Offline Files feature must be enabled.</span></span>

## <a name="examples"></a><span data-ttu-id="2d2fc-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="2d2fc-110">Examples</span></span>

<span data-ttu-id="2d2fc-111">L’exemple suivant illustre l’utilisation correcte de **Synchronize** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-111">The following example shows the proper use of **Synchronize** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2d2fc-112">Langage</span><span class="sxs-lookup"><span data-stu-id="2d2fc-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



<span data-ttu-id="2d2fc-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="2d2fc-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="2d2fc-114">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="2d2fc-114">Visual Basic:</span></span>


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2d2fc-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2d2fc-115">Requirements</span></span>



| <span data-ttu-id="2d2fc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d2fc-116">Requirement</span></span> | <span data-ttu-id="2d2fc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d2fc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2fc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d2fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d2fc-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d2fc-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d2fc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d2fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d2fc-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d2fc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2d2fc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d2fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d2fc-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d2fc-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2d2fc-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="2d2fc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d2fc-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d2fc-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2d2fc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2fc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d2fc-127"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2d2fc-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d2fc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d2fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2fc-129">**Dossier2**</span><span class="sxs-lookup"><span data-stu-id="2d2fc-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="2d2fc-130">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="2d2fc-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




