---
description: Appelée en réponse à la barricade d’affichage Web qui est ignorée par l’utilisateur.
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: Dossier2. DismissedWebViewBarricade, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115518"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="17bdf-103">Dossier2. DismissedWebViewBarricade, méthode</span><span class="sxs-lookup"><span data-stu-id="17bdf-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="17bdf-104">Appelée en réponse à la barricade d’affichage Web qui est ignorée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17bdf-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="17bdf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17bdf-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="17bdf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17bdf-106">Parameters</span></span>

<span data-ttu-id="17bdf-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="17bdf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17bdf-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17bdf-108">Return value</span></span>

<span data-ttu-id="17bdf-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="17bdf-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17bdf-110">Notes</span><span class="sxs-lookup"><span data-stu-id="17bdf-110">Remarks</span></span>

<span data-ttu-id="17bdf-111">Une application appelle cette méthode une fois que l’utilisateur a quitté l’affichage Web barricade.</span><span class="sxs-lookup"><span data-stu-id="17bdf-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="17bdf-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="17bdf-112">Examples</span></span>

<span data-ttu-id="17bdf-113">L’exemple suivant utilise **DismissedWebViewBarricade** pour spécifier que la barricade d’affichage Web pour le dossier C : \\ Windows a été fermée.</span><span class="sxs-lookup"><span data-stu-id="17bdf-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="17bdf-114">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="17bdf-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="17bdf-115">Langage</span><span class="sxs-lookup"><span data-stu-id="17bdf-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="17bdf-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="17bdf-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="17bdf-117">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="17bdf-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="17bdf-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="17bdf-118">Requirements</span></span>



| <span data-ttu-id="17bdf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17bdf-119">Requirement</span></span> | <span data-ttu-id="17bdf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="17bdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17bdf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17bdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="17bdf-122">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17bdf-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17bdf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17bdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="17bdf-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17bdf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="17bdf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="17bdf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="17bdf-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17bdf-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="17bdf-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="17bdf-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17bdf-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17bdf-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="17bdf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="17bdf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17bdf-130"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="17bdf-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17bdf-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17bdf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17bdf-132">**Dossier2**</span><span class="sxs-lookup"><span data-stu-id="17bdf-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="17bdf-133">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="17bdf-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




