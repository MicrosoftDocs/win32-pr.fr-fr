---
title: Méthode DeleteEx de la classe Win32_SessionBrokerFarmAccount
description: La \_ classe SessionBrokerFarmAccount Win32 n’est plus disponible pour une utilisation à partir de Windows Server 2012. | Méthode DeleteEx de la classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteEx
- Services Bureau à distance de la méthode DeleteEx, classe Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount de la classe Services Bureau à distance, méthode DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531272"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Méthode DeleteEx de la \_ classe Win32 SessionBrokerFarmAccount

\[La [**classe \_ SessionBrokerFarmAccount Win32**](win32-sessionbrokerfarmaccount.md) n’est plus disponible pour une utilisation à partir de Windows Server 2012.\]

Supprime le compte de batterie de serveurs.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DeleteComputerObject* \[ dans\]
</dt> <dd>

Indique si l’objet ordinateur associé à la batterie de serveurs doit être supprimé de Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                              |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SessionBrokerFarmAccount Win32**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





