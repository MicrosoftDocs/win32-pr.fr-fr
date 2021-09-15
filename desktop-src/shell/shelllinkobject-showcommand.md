---
description: Obtient ou définit l’état d’affichage initial (dimensionné, réduit ou agrandi) de la commande du lien.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: ShellLinkObject. ShowCommand, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523320"
---
# <a name="shelllinkobjectshowcommand-property"></a>ShellLinkObject. ShowCommand, propriété

Obtient ou définit l’état d’affichage initial (dimensionné, réduit ou agrandi) de la commande du lien.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a>Valeur de la propriété

État d’affichage du lien. Il peut s’agir de l’une des valeurs suivantes :

<dt>



 (1)


</dt> <dd>

Active et affiche une fenêtre. Si la fenêtre est réduite ou agrandie, le système la restaure à sa taille et à sa position d’origine.

</dd> <dt>



 (2)


</dt> <dd>

Active la fenêtre et l’affiche sous forme de fenêtre réduite.

</dd> <dt>



 (3)


</dt> <dd>

Active la fenêtre et l’affiche sous la forme d’une fenêtre agrandie.

</dd> </dl>

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation appropriée de cette propriété dans JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
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
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
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
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
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
Private Sub fnShellLinkObjectShowCommandVB()
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
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
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
| Client minimal pris en charge<br/> | Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




