---
title: WebViewFolderContents. FocusedItem, propriété (shldisp. h)
description: Propriété WebViewFolderContents. FocusedItem-obtient un objet FolderItem qui représente l’élément ayant le focus d’entrée.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- propriété FocusedItem Windows héritée fonctionnalités d’environnement
- propriété FocusedItem héritée Windows fonctionnalités d’environnement, objet WebViewFolderContents
- objet WebViewFolderContents héritage Windows fonctionnalités d’environnement, propriété FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d9a22ac1529fc7f8f3880f53666e9835fae1088d3c7548abfa38a5f400061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114529"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a>WebViewFolderContents. FocusedItem, propriété

Obtient un objet [**FolderItem**](../shell/folderitem.md) qui représente l’élément ayant le focus d’entrée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a>Valeur de la propriété

Variable de type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet élément ayant le focus.

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation appropriée de cette propriété dans JScript incorporée en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

