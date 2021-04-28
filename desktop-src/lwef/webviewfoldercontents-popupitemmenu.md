---
title: Méthode WebViewFolderContents. PopupItemMenu (shldisp. h)
description: 'Méthode WebViewFolderContents. PopupItemMenu : crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.'
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Méthode PopupItemMenu fonctionnalités d’environnement Windows héritées
- Méthode PopupItemMenu fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, méthode PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102637"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>Méthode WebViewFolderContents. PopupItemMenu

Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* \[ dans\]
</dt> <dd>

Type : **variante**

Objet [**FolderItem**](../shell/folderitem.md) pour lequel le menu contextuel sera créé.

</dd> <dt>

*VX* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Position horizontale du menu, en coordonnées d’écran.

</dd> <dt>

*Vy* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Position verticale du menu, en coordonnées d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

Lorsque cette méthode est retournée, contient la chaîne de commande.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de **PopupItemMenu** pour JScript Embedded en html.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



 

