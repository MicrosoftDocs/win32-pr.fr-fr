---
title: Méthode EnableTransport de la classe Win32_TSGatewayServerSettings
description: Active ou désactive le transport spécifié.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableTransport
- Services Bureau à distance de la méthode EnableTransport, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08087c4a28b0867f7457bed597a71c5156ea968fb50f3f2509c8da5ef3057fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059597"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode EnableTransport de la \_ classe Win32 TSGatewayServerSettings

Active ou désactive le transport spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TransportType* \[ dans\]
</dt> <dd>

Spécifie le type de transport. Il doit s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Transport RPC sur HTTP.

</dd> <dt>

1
</dt> <dd>

Transport HTTP.

</dd> <dt>

2
</dt> <dd>

Transport UDP.

</dd> </dl> </dd> <dt>

*Activer* \[ dans\]
</dt> <dd>

Spécifie si le transport est activé ou désactivé.

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

 

 





