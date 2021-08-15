---
description: Récupère des détails sur un élément dans un dossier. Par exemple, sa taille, son type ou l’heure de sa dernière modification.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Méthode Folder. GetDetailsOf (shlobj \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c703150069bc839f2d20024c0de8f3197fba09c5c3571e3de818dec3f3d6737c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860327"
---
# <a name="foldergetdetailsof-method"></a>Folder. GetDetailsOf, méthode

Récupère des détails sur un élément dans un dossier. Par exemple, sa taille, son type ou l’heure de sa dernière modification.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* 
</dt> <dd>

Type : **variante**

Élément pour lequel les informations doivent être récupérées. Il doit s’agir d’un objet [**FolderItem**](folderitem.md) .

</dd> <dt>

*iColumn* 
</dt> <dd>

Type : **entier**

Valeur **entière** qui spécifie les informations à récupérer. Les informations disponibles pour un élément dépendent du dossier dans lequel il est affiché. Cette valeur correspond au numéro de colonne de base zéro affiché dans une vue de l’interpréteur de commandes. Pour un élément dans le système de fichiers, il peut s’agir de l’une des valeurs suivantes :

<dt>



  (0)


</dt> <dd>

Récupère le nom de l’élément.

</dd> <dt>



 (1)


</dt> <dd>

Récupère la taille de l’élément.

</dd> <dt>



 (2)


</dt> <dd>

Récupère le type de l’élément.

</dd> <dt>



 (3)


</dt> <dd>

Récupère la date et l’heure de la dernière modification de l’élément.

</dd> <dt>



 (4)


</dt> <dd>

Récupère les attributs de l’élément.

</dd> <dt>



 (-1)


</dt> <dd>

Récupère les informations d’info-bulle pour l’élément.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Chaîne contenant le détail récupéré.

## <a name="remarks"></a>Remarques

> [!Note]  
> Toutes les méthodes ne sont pas implémentées pour tous les dossiers. Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL). Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.

 

## <a name="examples"></a>Exemples

L’exemple suivant utilise **GetDetailsOf** pour récupérer le type du fichier nommé Clock.avi. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
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
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
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
| En-tête<br/>                   | <dl> <dt>Shlobj \_ Core. h (include shldisp. h)</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
