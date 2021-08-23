---
title: WebViewFolderContents. ViewOptions, propriété (shldisp. h)
description: Obtient un jeu d’indicateurs ShellFolderViewOptions qui indiquent les options actuelles de la vue.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- propriété ViewOptions Windows héritée fonctionnalités d’environnement
- propriété ViewOptions héritée Windows fonctionnalités d’environnement, objet WebViewFolderContents
- objet WebViewFolderContents héritage Windows fonctionnalités d’environnement, propriété ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c897c75eab32962a18981c605c8465630aaf7b0c6b7d3e3f9a4fbe8e3d75d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607739"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>WebViewFolderContents. ViewOptions, propriété

Obtient un jeu d’indicateurs [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) qui indiquent les options actuelles de la vue.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valeur de la propriété

Variable de type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet d’options de vue.

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation appropriée de cette propriété dans JScript incorporée en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



 

