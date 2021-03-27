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
# <a name="folder2offlinestatus-property"></a>Dossier2. OfflineStatus, propriété

Contient l’état hors connexion du dossier.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Valeur de la propriété

**Entier** défini sur l’une des valeurs suivantes.

<dt>



 (OFS \_ DIRTYCACHE)


</dt> <dd>

Le serveur est en ligne avec des modifications non synchronisées.

</dd> <dt>



 (OFS \_ INACTIVE


</dt> <dd>

La mise en cache hors connexion n’est pas activée pour ce dossier.

</dd> <dt>



 (OFS \_ HORS connexion


</dt> <dd>

Le serveur est hors connexion.

</dd> <dt>



 (OFS \_ SERVICE


</dt> <dd>

Le serveur est en ligne.

</dd> <dt>



 (OFS \_ SERVERBACK)


</dt> <dd>

Le serveur est hors connexion, mais peut être atteint.

</dd> </dl>

## <a name="remarks"></a>Notes

> [!Note]  
> Les Fichiers hors connexion doivent être activés par le biais des options de dossier pour que **OfflineStatus** fonctionne correctement. Si l’option Fichiers hors connexion n’est pas activée, la propriété retourne **OFS \_ inactive**.

 

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de **OfflineStatus** pour JScript, VBScript et Visual Basic.

Langage


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



VBScript


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



Visual Basic :


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Dossier2**](folder2-object.md)
</dt> <dt>

[**Dossier**](folder.md)
</dt> </dl>

 

 




