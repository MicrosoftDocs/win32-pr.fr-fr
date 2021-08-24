---
title: Méthode SelectNetworkAdapter de la classe Win32_TSVirtualIP
description: Définit l’adresse MAC de la carte réseau à utiliser pour la virtualisation IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SelectNetworkAdapter
- Services Bureau à distance de la méthode SelectNetworkAdapter, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d27df38f8314720c4ed16d675cdbd06424611d2ccd127a45069586875c82d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865519"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Méthode SelectNetworkAdapter de la \_ classe Win32 TSVirtualIP

Définit l’adresse MAC de la carte réseau à utiliser pour la virtualisation IP.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NetworkAdapterMacAddress* \[ dans\]
</dt> <dd>

Type : **chaîne**

Spécifie l’adresse MAC de la carte réseau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

Si l’adresse MAC n’est pas valide ou n’existe pas, ou si le mode de virtualisation IP est par session, une erreur est retournée.

La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





