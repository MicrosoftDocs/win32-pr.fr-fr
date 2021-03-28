---
description: Recherche la cible d’un lien de Shell, même si la cible a été déplacée ou renommée.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: ShellLinkObject. Resolve, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973771"
---
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="1329b-103">ShellLinkObject. Resolve, méthode</span><span class="sxs-lookup"><span data-stu-id="1329b-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="1329b-104">Recherche la cible d’un lien de Shell, même si la cible a été déplacée ou renommée.</span><span class="sxs-lookup"><span data-stu-id="1329b-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1329b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1329b-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="1329b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1329b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1329b-107">*fFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1329b-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1329b-108">Type : **entier**</span><span class="sxs-lookup"><span data-stu-id="1329b-108">Type: **Integer**</span></span>

<span data-ttu-id="1329b-109">Indicateurs qui spécifient l’action à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="1329b-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="1329b-110">Il peut s’agir d’une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1329b-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="1329b-111">(1)</span><span class="sxs-lookup"><span data-stu-id="1329b-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-112">N’affiche pas de boîte de dialogue si le lien ne peut pas être résolu.</span><span class="sxs-lookup"><span data-stu-id="1329b-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="1329b-113">Lorsque cet indicateur est défini, le mot de poids fort de *fFlags* spécifie un délai d’attente, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="1329b-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="1329b-114">La méthode retourne si le lien ne peut pas être résolu dans le délai d’attente imparti.</span><span class="sxs-lookup"><span data-stu-id="1329b-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="1329b-115">Si le mot de poids fort est défini sur zéro, la durée d’expiration par défaut est de 3000 millisecondes (3 secondes).</span><span class="sxs-lookup"><span data-stu-id="1329b-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="1329b-116">(4)</span><span class="sxs-lookup"><span data-stu-id="1329b-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-117">Si le lien a été modifié, mettez à jour son chemin d’accès et sa liste d’identificateurs.</span><span class="sxs-lookup"><span data-stu-id="1329b-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="1329b-118">(8)</span><span class="sxs-lookup"><span data-stu-id="1329b-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-119">Ne mettez pas à jour les informations de lien.</span><span class="sxs-lookup"><span data-stu-id="1329b-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="1329b-120">(16)</span><span class="sxs-lookup"><span data-stu-id="1329b-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-121">N’exécutez pas l’heuristique de recherche.</span><span class="sxs-lookup"><span data-stu-id="1329b-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="1329b-122">(32)</span><span class="sxs-lookup"><span data-stu-id="1329b-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-123">N’utilisez pas le suivi des liaisons distribuées.</span><span class="sxs-lookup"><span data-stu-id="1329b-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="1329b-124">(64)</span><span class="sxs-lookup"><span data-stu-id="1329b-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-125">Désactivez le suivi des liaisons distribuées.</span><span class="sxs-lookup"><span data-stu-id="1329b-125">Disable distributed link tracking.</span></span> <span data-ttu-id="1329b-126">Par défaut, le suivi de lien distribué effectue le suivi des médias amovibles sur plusieurs appareils en fonction du nom du volume.</span><span class="sxs-lookup"><span data-stu-id="1329b-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="1329b-127">Il utilise également le chemin d’accès UNC pour effectuer le suivi des systèmes de fichiers distants dont la lettre de lecteur a changé.</span><span class="sxs-lookup"><span data-stu-id="1329b-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="1329b-128">La définition de cet indicateur désactive les deux types de suivi.</span><span class="sxs-lookup"><span data-stu-id="1329b-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="1329b-129">(128)</span><span class="sxs-lookup"><span data-stu-id="1329b-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="1329b-130">Appelez la Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1329b-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1329b-131">Notes</span><span class="sxs-lookup"><span data-stu-id="1329b-131">Remarks</span></span>

<span data-ttu-id="1329b-132">Cette méthode est fondamentalement identique dans les fonctionnalités à [**résoudre**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="1329b-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="1329b-133">Pour plus d’informations sur la résolution de liens, consultez la section Notes de cette page.</span><span class="sxs-lookup"><span data-stu-id="1329b-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="1329b-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="1329b-134">Examples</span></span>

<span data-ttu-id="1329b-135">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1329b-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1329b-136">Langage</span><span class="sxs-lookup"><span data-stu-id="1329b-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="1329b-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="1329b-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1329b-138">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="1329b-138">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1329b-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1329b-139">Requirements</span></span>



| <span data-ttu-id="1329b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1329b-140">Requirement</span></span> | <span data-ttu-id="1329b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="1329b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1329b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1329b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1329b-143">Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1329b-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1329b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1329b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1329b-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1329b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1329b-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="1329b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1329b-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1329b-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1329b-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="1329b-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1329b-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1329b-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1329b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="1329b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1329b-151"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1329b-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
