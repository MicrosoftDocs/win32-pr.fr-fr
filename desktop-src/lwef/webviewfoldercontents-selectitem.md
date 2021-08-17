---
title: Méthode WebViewFolderContents. SelectItem (shldisp. h)
description: Méthode WebViewFolderContents. SelectItem-définit l’état de sélection d’un élément dans la vue.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- fonctionnalités d’environnement Windows héritées de la méthode SelectItem
- méthode SelectItem héritage Windows fonctionnalités d’environnement, objet WebViewFolderContents
- objets WebViewFolderContents hérités Windows (fonctionnalités d’environnement), méthode SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d144801e62962f4071b6c8e60147326908a9b4f7787e0d4ac549be9c51fa3c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960619"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Méthode WebViewFolderContents. SelectItem

Définit l’état de sélection d’un élément dans la vue.

## <a name="syntax"></a>Syntaxe


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* \[ dans\]
</dt> <dd>

Type : **variante \***

Objet [**FolderItem**](../shell/folderitem.md) pour lequel l’état de sélection sera défini.

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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript incorporée en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



 

