---
title: Méthode SetVirtualizeLoopbackAddressesEnabled de la classe Win32_TSVirtualIP
description: Définit la valeur de la propriété VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualizeLoopbackAddressesEnabled
- Services Bureau à distance de la méthode SetVirtualizeLoopbackAddressesEnabled, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510525"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Méthode SetVirtualizeLoopbackAddressesEnabled de la \_ classe Win32 TSVirtualIP

Définit la valeur de la propriété **VirtualizeLoopbackAddressesEnabled** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[ dans\]
</dt> <dd>

Spécifie s’il faut activer la virtualisation des adresses de bouclage. Il peut s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

N’activez pas la virtualisation des adresses de bouclage.

</dd> <dt>

1
</dt> <dd>

Activez la virtualisation des adresses de bouclage.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





