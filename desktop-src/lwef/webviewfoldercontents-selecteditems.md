---
title: WebViewFolderContents.SelectedItems, méthode (Shldisp.h)
description: Obtient un objet FolderItems qui représente tous les éléments sélectionnés dans la vue.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- SelectedItems, méthode fonctionnalités d’environnement Windows héritées
- SelectedItems, méthode fonctionnalités d’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, SelectedItems, méthode
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033169"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>WebViewFolderContents. SelectedItems, méthode

Obtient un objet [**FolderItems**](../shell/folderitems.md) qui représente tous les éléments sélectionnés dans la vue.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **FolderItems**](../shell/folderitems.md)\*\***

Référence d’objet à l’objet [**FolderItems**](../shell/folderitems.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

