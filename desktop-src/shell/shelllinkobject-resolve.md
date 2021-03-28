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
# <a name="shelllinkobjectresolve-method"></a>ShellLinkObject. Resolve, méthode

Recherche la cible d’un lien de Shell, même si la cible a été déplacée ou renommée.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fFlags* \[ dans\]
</dt> <dd>

Type : **entier**

Indicateurs qui spécifient l’action à entreprendre. Il peut s’agir d’une combinaison des valeurs suivantes :

<dt>



 (1)


</dt> <dd>

N’affiche pas de boîte de dialogue si le lien ne peut pas être résolu. Lorsque cet indicateur est défini, le mot de poids fort de *fFlags* spécifie un délai d’attente, en millisecondes. La méthode retourne si le lien ne peut pas être résolu dans le délai d’attente imparti. Si le mot de poids fort est défini sur zéro, la durée d’expiration par défaut est de 3000 millisecondes (3 secondes).

</dd> <dt>



 (4)


</dt> <dd>

Si le lien a été modifié, mettez à jour son chemin d’accès et sa liste d’identificateurs.

</dd> <dt>



 (8)


</dt> <dd>

Ne mettez pas à jour les informations de lien.

</dd> <dt>



 (16)


</dt> <dd>

N’exécutez pas l’heuristique de recherche.

</dd> <dt>



 (32)


</dt> <dd>

N’utilisez pas le suivi des liaisons distribuées.

</dd> <dt>



 (64)


</dt> <dd>

Désactivez le suivi des liaisons distribuées. Par défaut, le suivi de lien distribué effectue le suivi des médias amovibles sur plusieurs appareils en fonction du nom du volume. Il utilise également le chemin d’accès UNC pour effectuer le suivi des systèmes de fichiers distants dont la lettre de lecteur a changé. La définition de cet indicateur désactive les deux types de suivi.

</dd> <dt>



 (128)


</dt> <dd>

Appelez la Windows Installer.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Cette méthode est fondamentalement identique dans les fonctionnalités à [**résoudre**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve). Pour plus d’informations sur la résolution de liens, consultez la section Notes de cette page.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript, VBScript et Visual Basic.

Langage


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



VBScript


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



Visual Basic :


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
