---
description: 'Méthode IShellDispatch2. ServiceStop : arrête un service nommé.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Méthode IShellDispatch2. ServiceStop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 71bc0502d45e4092decfe1b712ed11f75a02bf50d112436ad1d21f9e02c17e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221020"
---
# <a name="ishelldispatch2servicestop-method"></a>Méthode IShellDispatch2. ServiceStop

Arrête un service nommé.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
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

Affectez la valeur **true** pour que le service soit démarré par le gestionnaire de contrôle des services lors de l’appel de [**ServiceStart**](ishelldispatch2-servicestart.md) . Pour que la configuration du service reste inchangée, affectez à *vPersistent* la valeur **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Type : **variante \***

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

### <a name="vb"></a>VB

Type : **variante \***

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Remarques

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ServiceStop**](./shell-servicestop.md) .

La méthode retourne la **valeur false** si le service a déjà été arrêté. Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **ServiceStop** pour arrêter le service Messenger. l’utilisation est indiquée pour JScript et VBScript.

JScript :


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

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



 

 
