---
description: 'Méthode IShellDispatch. Open : ouvre le dossier spécifié.'
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: IShellDispatch. Open, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4b5301e030926b9bcfdc18949b6a04706c22bb71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086627"
---
# <a name="ishelldispatchopen-method"></a>IShellDispatch. Open, méthode

Ouvre le dossier spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*vdir* \[ dans\]
</dt> <dd>

Type : **variante**

Chaîne qui spécifie le chemin d’accès au dossier ou l’une des valeurs [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Notez que les noms de constantes trouvés dans **ShellSpecialFolderConstants** sont disponibles dans Visual Basic, mais pas dans VBScript ou JScript. Dans ce cas, les valeurs numériques doivent être utilisées à leur place.

Si *vdir* est défini sur l’un des [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) et que le dossier spécial n’existe pas, cette fonction crée le dossier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Open**](shell-open.md) .

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **Open** dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**Explorer**](shell-explore.md)
</dt> </dl>

 

 




