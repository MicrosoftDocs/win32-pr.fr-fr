---
title: Méthode GetIPAndPort de la classe Win32_TSGatewayServerSettings
description: Obtient l’adresse IP d’écoute et le numéro de port pour le transport spécifié.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetIPAndPort
- Services Bureau à distance de la méthode GetIPAndPort, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317161"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode GetIPAndPort de la \_ classe Win32 TSGatewayServerSettings

Obtient l’adresse IP d’écoute et le numéro de port pour le transport spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
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

*Adresse IP* \[ à\]
</dt> <dd>

Chaîne qui reçoit l’adresse IP d’écoute, sous forme d’octet (par exemple, « 192.168.1.1 »).

</dd> <dt>

*Port* \[ à\]
</dt> <dd>

Spécifie le numéro de port d’écoute.

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

 

 





