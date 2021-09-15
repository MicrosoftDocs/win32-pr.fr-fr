---
description: ajoute un nouveau canal à la liste de canaux dans le Windows menu favoris d’Internet Explorer et à la barre de canaux sur le bureau.
title: Méthode ShellUIHelper. AddChannel (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525357"
---
# <a name="shelluihelperaddchannel-method"></a>Méthode ShellUIHelper. AddChannel

ajoute un nouveau canal à la liste de canaux dans le Windows menu **favoris** d’Internet Explorer et à la barre de **canaux** sur le bureau.

> [!Note]  
> cette méthode n’est plus prise en charge sous Windows Vista. Dans ce système d’exploitation, il renvoie E \_ NOTIMPL.

 

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*surl* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valeur de **chaîne** qui spécifie l’URL du fichier CDF.

> [!Note]  
> Les liens contenus dans le fichier CDF doivent utiliser des protocoles HTTP, HTTPs ou FTP. Si le fichier CDF contient un autre protocole, l’ajout du canal échoue et aucune boîte de dialogue ne s’affiche.

 

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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



Visual Basic :


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
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



 

 
