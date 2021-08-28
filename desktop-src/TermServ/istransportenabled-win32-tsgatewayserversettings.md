---
title: Méthode IsTransportEnabled de la classe Win32_TSGatewayServerSettings
description: Détermine si le transport spécifié est activé.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsTransportEnabled
- Services Bureau à distance de la méthode IsTransportEnabled, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7960748228e11f3749cd86daa2a323ca32ab9b05e1c17f98261ad4ae62b0fc9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515079"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode IsTransportEnabled de la \_ classe Win32 TSGatewayServerSettings

Détermine si le transport spécifié est activé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
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

*Activé* \[ à\]
</dt> <dd>

Valeur **booléenne** qui indique si le transport est activé.

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

 

 





