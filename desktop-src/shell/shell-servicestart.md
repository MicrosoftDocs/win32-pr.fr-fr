---
description: Méthode Shell. ServiceStart-démarre un service nommé.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Shell. ServiceStart, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: afdc1e7cac8d50de08e21cfad5cb492b5b51dcb647e963b4c003e9600a924244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709549"
---
# <a name="shellservicestart-method"></a>Shell. ServiceStart, méthode

Démarre un service nommé.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sServiceName* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient le nom du service.

</dd> <dt>

*vPersistent* \[ dans\]
</dt> <dd>

Type : **variante**

Affectez la valeur **true** pour que le service démarre automatiquement par le gestionnaire de contrôle des services lors du démarrage du système. Affectez la valeur **false** pour que la configuration du service reste inchangée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Type : **variante \***

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

### <a name="vb"></a>VB

Type : **variante \***

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Remarques

La méthode retourne la **valeur false** si le service a déjà été démarré. Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **ServiceStart** pour démarrer le service Messenger. l’utilisation est indiquée pour JScript et VBScript.

JScript :


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



VBScript


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
