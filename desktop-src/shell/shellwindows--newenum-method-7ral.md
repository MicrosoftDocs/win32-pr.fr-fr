---
description: Crée et retourne un nouvel objet ShellWindows qui est une copie de cet objet ShellWindows.
title: Méthode ShellWindows._NewEnum (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: 696767844e2cc5dbe17aa44c2f76a8b0550b86115437e0d5f3e1f1f2543dbb2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857098"
---
# <a name="shellwindows_newenum-method"></a>ShellWindows. \_ NewEnum, méthode

Crée et retourne un nouvel objet [**ShellWindows**](shellwindows.md) qui est une copie de cet objet **ShellWindows** .

## <a name="syntax"></a>Syntaxe


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Référence d’objet à la copie de l’objet [**ShellWindows**](shellwindows.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre la **\_ NewEnum** en cours d’utilisation. L’utilisation appropriée est indiquée pour VBScript et Visual Basic. Cette méthode ne peut pas être utilisée avec JScript.

VBScript


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
