---
description: Affiche l’interface utilisateur par défaut pour la création d’un élément favori. L’interface utilisateur est initialisée avec les paramètres spécifiés.
title: Méthode ShellUIHelper. AddFavorite (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973734"
---
# <a name="shelluihelperaddfavorite-method"></a>Méthode ShellUIHelper. AddFavorite

Affiche l’interface utilisateur par défaut pour la création d’un élément favori. L’interface utilisateur est initialisée avec les paramètres spécifiés.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*surl* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valeur de **chaîne** qui spécifie l’URL de l’élément à ajouter au dossier **favoris** .

</dd> <dt>

*vTitle* \[ dans, facultatif\]
</dt> <dd>

Type : **Variant \** _

Valeur _ *Variant** qui spécifie le nom de l’élément.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML et Visual Basic.

Langage


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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



Visual Basic :


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
