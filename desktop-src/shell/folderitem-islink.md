---
description: Indique si l’élément est un raccourci.
ms.assetid: f3400f0b-5c7f-4d41-a162-1c35014082ac
title: FolderItem. IsLink, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: eb12c2273bb22af2df9f76c6606cad69223fa04292e0d556a65d4898bc968c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093123"
---
# <a name="folderitemislink-property"></a>FolderItem. IsLink, propriété

Indique si l’élément est un raccourci.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
bIsLink = FolderItem.IsLink
```



## <a name="property-value"></a>Valeur de la propriété

Valeur **booléenne** qui reçoit la **valeur true** si l’élément est un raccourci ou **false** dans le cas contraire.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **IsLink** pour déterminer si un objet particulier est un lien. Dans ce cas, l’objet est un raccourci vers Internet Explorer et doit donc retourner la **valeur true**. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnIsLinkJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfPROGRAMS = 2;
        
        objFolder2 = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsLink;
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsLinkVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfPROGRAMS
                
            ssfPROGRAMS = 2
            set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsLink
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnIsLinkVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsLink
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




