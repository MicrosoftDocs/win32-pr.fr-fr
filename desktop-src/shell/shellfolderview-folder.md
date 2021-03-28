---
description: Obtient un objet dossier qui représente la vue.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: ShellFolderView. Folder, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40590064048ba5410dc9341791aec443f16d68e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209943"
---
# <a name="shellfolderviewfolder-property"></a>ShellFolderView. Folder, propriété

Obtient un objet [**dossier**](folder.md) qui représente la vue.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a>Valeur de la propriété

Objet qui reçoit l’objet [**Folder**](folder.md) .

## <a name="remarks"></a>Notes

Le **dossier** ne peut être appelé que sur le système local. Elle ne fonctionnera pas lorsqu’elle sera exécutée sur une page Web via HTTP ou UNC.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de cette propriété pour JScript Embedded en HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




