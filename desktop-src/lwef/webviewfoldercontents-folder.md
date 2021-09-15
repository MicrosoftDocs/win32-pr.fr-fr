---
title: WebViewFolderContents.Folder, propriété (Shldisp.h)
description: WebViewFolderContents. Folder, propriété-obtient un objet Folder qui représente la vue.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- propriétés de dossier héritage Windows fonctionnalités d’environnement
- propriété de dossier héritage Windows fonctionnalités d’environnement, objet WebViewFolderContents
- objet WebViewFolderContents héritage Windows fonctionnalités d’environnement, propriété de dossier
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522540"
---
# <a name="webviewfoldercontentsfolder-property"></a>WebViewFolderContents. Folder, propriété

Obtient un objet [**dossier**](../shell/folder.md) qui représente la vue.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>Valeur de la propriété

Objet qui reçoit l’objet [**Folder**](../shell/folder.md) .

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation appropriée de cette propriété dans JScript incorporée en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

