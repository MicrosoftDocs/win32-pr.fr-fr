---
description: Méthode ShellFolderView. SelectItem-définit l’état de sélection d’un élément dans la vue.
title: Méthode ShellFolderView. SelectItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116747"
---
# <a name="shellfolderviewselectitem-method"></a>Méthode ShellFolderView. SelectItem

Définit l’état de sélection d’un élément dans la vue.

## <a name="syntax"></a>Syntaxe


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* \[ dans\]
</dt> <dd>

Type : **variante \***

Objet [**FolderItem**](folderitem.md) pour lequel l’état de sélection sera défini.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Type : **entier**

Ensemble d’indicateurs qui indiquent le nouvel état de sélection. Il peut s’agir d’une ou plusieurs des valeurs suivantes.

<dt>



  (0)


</dt> <dd>

Désélectionnez l’élément.

</dd> <dt>



 (1)


</dt> <dd>

Sélectionnez l’élément.

</dd> <dt>



 (3)


</dt> <dd>

Mettez l’élément en mode édition.

</dd> <dt>



 (4)


</dt> <dd>

Désélectionner tout sauf l’élément spécifié.

</dd> <dt>



 (8)


</dt> <dd>

Vérifiez que l’élément est affiché dans la vue.

</dd> <dt>



 (16)


</dt> <dd>

Donne le focus à l’élément.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

[**FocusedItem**](shellfolderview-focuseditem.md) peut uniquement être appelé sur le système local. Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de cette méthode dans JScript incorporé en HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




