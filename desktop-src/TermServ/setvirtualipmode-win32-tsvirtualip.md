---
title: Méthode SetVirtualIPMode de la classe Win32_TSVirtualIP
description: Définit la valeur de la propriété VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualIPMode
- Services Bureau à distance de la méthode SetVirtualIPMode, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513616"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a>Méthode SetVirtualIPMode de la \_ classe Win32 TSVirtualIP

Définit la valeur de la propriété **VirtualIPMode** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VirtualIPMode* \[ dans\]
</dt> <dd>

Type : **UInt32**

Spécifie le mode de virtualisation IP utilisé sur le serveur. Il peut s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Le mode de virtualisation IP est par session.

</dd> <dt>

1
</dt> <dd>

Le mode de virtualisation IP est par utilisateur.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

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

 

 





