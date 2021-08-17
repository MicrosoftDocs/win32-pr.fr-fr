---
title: Méthode SetIPAndPort de la classe Win32_TSGatewayServerSettings
description: Définit l’adresse IP d’écoute et le numéro de port pour le transport spécifié.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetIPAndPort
- Services Bureau à distance de la méthode SetIPAndPort, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40c52523869e07268a26d858e0e70b933431a6583998c9d0041f476678d243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137972"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode SetIPAndPort de la \_ classe Win32 TSGatewayServerSettings

Définit l’adresse IP d’écoute et le numéro de port pour le transport spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
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

*Adresse IP* \[ dans\]
</dt> <dd>

Spécifie l’adresse IP d’écoute, sous forme d’octet (par exemple, « 192.168.1.1 »).

</dd> <dt>

*Port* \[ dans\]
</dt> <dd>

Spécifie le numéro de port d’écoute.

</dd> <dt>

*OverrideExisting* \[ dans\]
</dt> <dd>

Indique s’il faut remplacer la liaison de port/adresse IP existante pour HTTP. Ce paramètre est utilisé uniquement si le paramètre *TransportType* contient 0 (RPC sur http) ou 1 (http).

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

 

 





