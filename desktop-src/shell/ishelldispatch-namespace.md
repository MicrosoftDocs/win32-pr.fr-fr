---
description: 'Méthode IShellDispatch. NameSpace : crée et retourne un objet Folder pour le dossier spécifié.'
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Méthode IShellDispatch. NameSpace (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100517"
---
# <a name="ishelldispatchnamespace-method"></a>IShellDispatch. NameSpace, méthode

Crée et retourne un objet [**Folder**](folder.md) pour le dossier spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*vdir* \[ dans\]
</dt> <dd>

Type : **variante**

Dossier pour lequel créer l’objet [**dossier**](folder.md) . Il peut s’agir d’une chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript. Dans ce cas, les valeurs numériques doivent être utilisées à leur place.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Type : **[ **dossier**](folder.md)\*\***

Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié. Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.

### <a name="vb"></a>VB

Type : **[ **dossier**](folder.md)\*\***

Référence d’objet à l’objet [**dossier**](folder.md) pour le dossier spécifié. Si le dossier n’est pas créé avec succès, cette valeur retourne **null**.

## <a name="remarks"></a>Notes 

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Namespace**](shell-namespace.md) .

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de l' [**espace de noms**](shell-namespace.md) dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




