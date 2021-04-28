---
description: 'Shell. CanStartStopService, méthode : détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.'
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Shell. CanStartStopService, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083687"
---
# <a name="shellcanstartstopservice-method"></a>Shell. CanStartStopService, méthode

Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sServiceName* \[ dans\]
</dt> <dd>

Type : **chaîne**

**Chaîne** qui contient le nom du service.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Type : **variante \***

Retourne la **valeur true** si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.

### <a name="vb"></a>VB

Type : **variante \***

Retourne la **valeur true** si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.

## <a name="remarks"></a>Notes 

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **CanStartStopService** pour JScript et VBScript.

Langage


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




