---
title: Méthode SetEnforceChannelBinding de la classe Win32_TSGatewayServerSettings
description: Définit la propriété EnforceChannelBinding.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEnforceChannelBinding
- Services Bureau à distance de la méthode SetEnforceChannelBinding, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetEnforceChannelBinding
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a2e076fb4ba439faa7cc22f30da1f815b0571ede0477b875e25176a7f0297e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988029"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode SetEnforceChannelBinding de la \_ classe Win32 TSGatewayServerSettings

Définit la propriété **EnforceChannelBinding** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EnforceChannelBinding* \[ dans\]
</dt> <dd>

Spécifie la nouvelle valeur de la propriété **EnforceChannelBinding** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





