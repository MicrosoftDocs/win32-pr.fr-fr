---
title: WebViewFolderContents.SelectedItems, méthode (Shldisp.h)
description: WebViewFolderContents. SelectedItems, méthode-obtient un objet FolderItems qui représente tous les éléments sélectionnés dans la vue.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- fonctions de l’environnement Windows héritées de la méthode SelectedItems
- SelectedItems, méthode héritage Windows fonctionnalités d’environnement, objet WebViewFolderContents
- objets WebViewFolderContents hérités (fonctionnalités de l’environnement Windows), SelectedItems, méthode
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
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292287"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>WebViewFolderContents. SelectedItems, méthode

Obtient un objet [**FolderItems**](../shell/folderitems.md) qui représente tous les éléments sélectionnés dans la vue.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **FolderItems**](../shell/folderitems.md)\*\***

Référence d’objet à l’objet [**FolderItems**](../shell/folderitems.md) .

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript incorporée en HTML.


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

