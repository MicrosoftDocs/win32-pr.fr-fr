---
title: Méthode SetDisableForcibleLogoff de la classe Win32_TerminalServiceSetting
description: Méthode SetDisableForcibleLogoff de la classe Win32_TerminalServiceSetting-cette méthode n’est pas prise en charge.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDisableForcibleLogoff
- Services Bureau à distance de la méthode SetDisableForcibleLogoff, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919616"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>Méthode SetDisableForcibleLogoff de la \_ classe Win32 TerminalServiceSetting

Cette méthode n'est pas prise en charge.

**Windows Vista et Windows Server 2008 :** Active ou désactive si un administrateur connecté à la console peut être déconnecté de force.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DisableForcibleLogoff* \[ dans\]
</dt> <dd>

Indicateur de désactivation ou d’activation de la propriété **DisableForcibleLogoff** , qui détermine si un administrateur connecté à la console peut être déconnecté de force.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Désactivez la propriété. L’administrateur connecté peut être déconnecté de force.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Activez la propriété. L’administrateur connecté ne peut pas être déconnecté de force.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Fin de la prise en charge des clients<br/>    | Windows Vista<br/>                                                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





