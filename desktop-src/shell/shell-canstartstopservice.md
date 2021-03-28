---
description: Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.
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
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952242"
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

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Type : **Variant \** _

Retourne _ *true** si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.

### <a name="vb"></a>VB

Type : **Variant \** _

Retourne _ *true** si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.

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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 




