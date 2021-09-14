---
description: Ajoute un élément à Microsoft Active Desktop.
title: Méthode ShellUIHelper. AddDesktopComponent (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196391"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Méthode ShellUIHelper. AddDesktopComponent

Ajoute un élément à Microsoft Active Desktop.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*surl* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valeur de **chaîne** qui spécifie l’URL du nouvel élément favori.

</dd> <dt>

*sSpécification* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valeur de **chaîne** qui spécifie le type d’élément ajouté. Il peut s’agir de l’une des valeurs suivantes.

<dt>



 image


</dt> <dd>

Le composant est une image.

</dd> <dt>



 hameçonnage


</dt> <dd>

Le composant est un site Web.

</dd> </dl> </dd> <dt>

À *gauche* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Position du bord gauche du composant, en coordonnées d’écran.

</dd> <dt>

En *haut* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Position du bord supérieur du composant, en coordonnées d’écran.

</dd> <dt>

*Largeur* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Largeur du composant, en unités d’écran.

</dd> <dt>

*Hauteur* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Hauteur du composant, en unités d’écran.

</dd> </dl>

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript incorporée en HTML et Visual Basic.

JScript :


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic :


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
