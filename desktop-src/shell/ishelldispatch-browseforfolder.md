---
description: 'Méthode IShellDispatch. BrowseForFolder : crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de renvoyer l’objet dossier sélectionné.'
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Méthode IShellDispatch. BrowseForFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e70fd50d4b08787326f93cddf7ec55a0eaacb25fa815cc2b4c8246c1934494a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551829"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>Méthode IShellDispatch. BrowseForFolder

Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet [**dossier**](folder.md) du dossier sélectionné.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Type : **entier**

Handle de la fenêtre parente de la boîte de dialogue. Cette valeur peut être zéro.

</dd> <dt>

*sTitle* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valeur de **chaîne** qui représente le titre affiché dans la boîte de dialogue **Parcourir** .

</dd> <dt>

*iOptions* \[ dans\]
</dt> <dd>

Type : **entier**

Valeur **entière** qui contient les options de la méthode. Il peut s’agir de zéro ou d’une combinaison des valeurs figurant dans le membre **ulFlags** de la structure [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .

</dd> <dt>

*vRootFolder* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Dossier racine à utiliser dans la boîte de dialogue. L’utilisateur ne peut pas parcourir plus haut dans l’arborescence que ce dossier. Si cette valeur n’est pas spécifiée, le dossier racine utilisé dans la boîte de dialogue est le bureau. Cette valeur peut être une chaîne qui spécifie le chemin d’accès du dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript. Dans ce cas, les valeurs numériques doivent être utilisées à leur place.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Type : **dossier \* \***

Référence d’objet à l’objet [**dossier**](folder.md) du dossier sélectionné.

### <a name="vb"></a>VB

Type : **dossier \* \***

Référence d’objet à l’objet [**dossier**](folder.md) du dossier sélectionné.

## <a name="remarks"></a>Remarques

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. BrowseForFolder**](shell-browseforfolder.md) .

## <a name="examples"></a>Exemples

les exemples suivants utilisent **BrowseForFolder** pour afficher une fenêtre de navigation intitulée « Example » enracinée dans le dossier Windows. l’utilisation est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
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



 

 
