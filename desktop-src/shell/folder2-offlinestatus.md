---
description: Contient l’état hors connexion du dossier.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Propriété dossier2. OfflineStatus (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971907"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="3aab2-103">Dossier2. OfflineStatus, propriété</span><span class="sxs-lookup"><span data-stu-id="3aab2-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="3aab2-104">Contient l’état hors connexion du dossier.</span><span class="sxs-lookup"><span data-stu-id="3aab2-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="3aab2-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3aab2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aab2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aab2-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="3aab2-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3aab2-107">Property value</span></span>

<span data-ttu-id="3aab2-108">**Entier** défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3aab2-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="3aab2-109">(OFS \_ DIRTYCACHE)</span><span class="sxs-lookup"><span data-stu-id="3aab2-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="3aab2-110">Le serveur est en ligne avec des modifications non synchronisées.</span><span class="sxs-lookup"><span data-stu-id="3aab2-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="3aab2-111">(OFS \_ INACTIVE</span><span class="sxs-lookup"><span data-stu-id="3aab2-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="3aab2-112">La mise en cache hors connexion n’est pas activée pour ce dossier.</span><span class="sxs-lookup"><span data-stu-id="3aab2-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="3aab2-113">(OFS \_ HORS connexion</span><span class="sxs-lookup"><span data-stu-id="3aab2-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="3aab2-114">Le serveur est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3aab2-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="3aab2-115">(OFS \_ SERVICE</span><span class="sxs-lookup"><span data-stu-id="3aab2-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="3aab2-116">Le serveur est en ligne.</span><span class="sxs-lookup"><span data-stu-id="3aab2-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="3aab2-117">(OFS \_ SERVERBACK)</span><span class="sxs-lookup"><span data-stu-id="3aab2-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="3aab2-118">Le serveur est hors connexion, mais peut être atteint.</span><span class="sxs-lookup"><span data-stu-id="3aab2-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3aab2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3aab2-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3aab2-120">Les Fichiers hors connexion doivent être activés par le biais des options de dossier pour que **OfflineStatus** fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="3aab2-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="3aab2-121">Si l’option Fichiers hors connexion n’est pas activée, la propriété retourne **OFS \_ inactive**.</span><span class="sxs-lookup"><span data-stu-id="3aab2-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3aab2-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="3aab2-122">Examples</span></span>

<span data-ttu-id="3aab2-123">L’exemple suivant illustre l’utilisation correcte de **OfflineStatus** pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3aab2-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3aab2-124">Langage</span><span class="sxs-lookup"><span data-stu-id="3aab2-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="3aab2-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="3aab2-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="3aab2-126">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="3aab2-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3aab2-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3aab2-127">Requirements</span></span>



| <span data-ttu-id="3aab2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aab2-128">Requirement</span></span> | <span data-ttu-id="3aab2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aab2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aab2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aab2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3aab2-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aab2-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3aab2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aab2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3aab2-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3aab2-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3aab2-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="3aab2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aab2-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aab2-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3aab2-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="3aab2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3aab2-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3aab2-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3aab2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3aab2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aab2-139"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3aab2-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aab2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aab2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aab2-141">**Dossier2**</span><span class="sxs-lookup"><span data-stu-id="3aab2-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="3aab2-142">**Dossier**</span><span class="sxs-lookup"><span data-stu-id="3aab2-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




