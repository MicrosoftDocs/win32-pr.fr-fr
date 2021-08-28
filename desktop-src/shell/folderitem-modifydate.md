---
description: Pour un fichier, définit ou obtient la date et l’heure de la dernière modification. Pour un dossier, récupère la date et l’heure de la dernière modification d’un dossier, mais ne peut pas le définir.
ms.assetid: bb60c800-863b-469b-b937-9816b8b338bf
title: FolderItem. ModifyDate, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.ModifyDate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06e6c0b4d8254b4e67ccf4f7d09afbedb662c122584f71bf2dea7e25005031aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937079"
---
# <a name="folderitemmodifydate-property"></a>FolderItem. ModifyDate, propriété

Pour un fichier, définit ou obtient la date et l’heure de la dernière modification. Pour un dossier, récupère la date et l’heure de la dernière modification d’un dossier, mais ne peut pas le définir.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
iModifyDate = FolderItem.ModifyDate
FolderItem.ModifyDate = iModifyDate
```



## <a name="property-value"></a>Valeur de la propriété

**Date** qui spécifie ou reçoit la date et l’heure de la dernière modification de l’élément.

## <a name="examples"></a>Exemples

l’exemple suivant utilise **ModifyDate** pour récupérer la date de dernière modification de Bloc-notes puis le réinitialiser à une heure très longue. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnModifyDateGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.ModifyDate;
                objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM";
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnModifyDateGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
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
Private Sub fnModifyDateGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
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



 

 




