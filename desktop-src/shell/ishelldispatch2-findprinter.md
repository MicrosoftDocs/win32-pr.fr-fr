---
description: 'Méthode IShellDispatch2. FindPrinter : affiche la boîte de dialogue Rechercher l’imprimante.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Méthode IShellDispatch2. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196472"
---
# <a name="ishelldispatch2findprinter-method"></a>Méthode IShellDispatch2. FindPrinter

Affiche la boîte de dialogue **Rechercher l’imprimante** .

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sName* \[ dans, facultatif\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient le nom de l’imprimante.

</dd> <dt>

*sLocation* \[ dans, facultatif\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient l’emplacement de l’imprimante.

</dd> <dt>

*sModel* \[ dans, facultatif\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient le modèle d’imprimante.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FindPrinter**](./shell-findprinter.md) .

Si vous assignez des chaînes à un ou plusieurs des paramètres facultatifs, ils s’affichent en tant que valeurs par défaut dans le contrôle d’édition associé lorsque la boîte de dialogue **Rechercher l’imprimante** est affichée. L’utilisateur peut accepter ou remplacer ces valeurs. Si aucune valeur n’est assignée à un paramètre, la zone d’édition associée est vide et l’utilisateur doit entrer une valeur.

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **FindPrinter** pour afficher la boîte de dialogue **Rechercher une imprimante** pour une application particulière. l’utilisation est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
