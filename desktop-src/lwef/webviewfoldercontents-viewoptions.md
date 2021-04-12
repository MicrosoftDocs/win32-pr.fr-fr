---
title: WebViewFolderContents. ViewOptions, propriété (shldisp. h)
description: Obtient un jeu d’indicateurs ShellFolderViewOptions qui indiquent les options actuelles de la vue.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Propriétés ViewOptions héritées fonctionnalités de l’environnement Windows
- Propriété ViewOptions fonctionnalités de l’environnement Windows héritées, objet WebViewFolderContents
- Objet WebViewFolderContents fonctionnalités d’environnement Windows héritées, propriété ViewOptions
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
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032446"
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

L’exemple suivant illustre l’utilisation correcte de cette propriété dans JScript Embedded en HTML.


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
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

