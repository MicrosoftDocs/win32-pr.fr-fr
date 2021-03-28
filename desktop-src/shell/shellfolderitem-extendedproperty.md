---
description: Obtient la valeur d’une propriété à partir du jeu de propriétés d’un élément. La propriété peut être spécifiée par nom ou par l’identificateur de format (FMTID) et l’identificateur de propriété (PID) du jeu de propriétés.
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Méthode ShellFolderItem. ExtendedProperty (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973591"
---
# <a name="shellfolderitemextendedproperty-method"></a>Méthode ShellFolderItem. ExtendedProperty

Obtient la valeur d’une propriété à partir du jeu de propriétés d’un élément. La propriété peut être spécifiée par nom ou par l’identificateur de format (FMTID) et l’identificateur de propriété (PID) du jeu de propriétés.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sPropName* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valeur de **chaîne** qui spécifie la propriété. Pour plus d'informations, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **Variant \** _

Lorsque cette méthode est retournée, contient la valeur de la propriété, si elle existe pour l’élément spécifié. La valeur aura un typage complet, par exemple, les dates sont retournées en tant que dates, et non en tant que chaînes.

Cette méthode retourne une chaîne de longueur nulle si la propriété est valide mais n’existe pas pour l’élément spécifié, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Il existe deux façons de spécifier une propriété. La première consiste à affecter le nom bien connu de la propriété, tel que « Author » ou « date », à _sPropName *. Toutefois, chaque propriété est membre d’un jeu de propriétés COM (Component Object Model) et peut également être identifiée en spécifiant son ID de format (FMTID) et son ID de propriété (PID). Un [**fmtid**](../stg/structured-storage-serialized-property-set-format.md) est un GUID qui identifie le jeu de propriétés, et un [**PID**](../stg/structured-storage-serialized-property-set-format.md) est un entier qui identifie une propriété particulière dans le jeu de propriétés.

La spécification d’une propriété par ses valeurs FMTID/PID est généralement plus efficace que l’utilisation de son nom. Pour utiliser les valeurs FMTID/PID d’une propriété avec **ExtendedProperty**, elles doivent être combinées dans un scid. Un SCID est une chaîne qui contient les valeurs FMTID/PID sous la forme «*fmtid * * PID*», où fmtid est le format de chaîne du GUID du jeu de propriétés. Par exemple, le SCID de la propriété auteur du jeu de propriétés des informations de résumé est « {F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4 ».

Pour obtenir la liste des FMTIDs et des PID actuellement pris en charge par l’interpréteur de commandes, consultez [**SHCOLUMNID**](./objects.md).

## <a name="examples"></a>Exemples

Cet exemple de code illustre comment utiliser **ExtendedProperty** pour récupérer les propriétés « Title » et « Author » à partir d’un document Word. Une fois que vous avez l’objet [**ShellFolderItem**](shellfolderitem-object.md) associé au fichier, *fiWordDoc* dans cet exemple, récupérez la valeur de la propriété en passant son nom à **ExtendedProperty**.


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Une approche plus rapide et plus efficace consiste à passer un SCID à **ExtendedProperty**.


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



Les exemples suivants illustrent l’utilisation appropriée de cette méthode pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
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
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
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
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
