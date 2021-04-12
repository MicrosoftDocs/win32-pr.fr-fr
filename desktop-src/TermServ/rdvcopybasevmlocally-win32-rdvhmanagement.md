---
title: Méthode RdvCopyBaseVmLocally de la classe Win32_RdvhManagement
description: Copie un ordinateur virtuel de base local sur un serveur hôte de virtualisation des services Bureau à distance (RDV) spécifié.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvCopyBaseVmLocally
- Services Bureau à distance de la méthode RdvCopyBaseVmLocally, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385171"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>Méthode RdvCopyBaseVmLocally de la \_ classe Win32 RdvhManagement

Copie un ordinateur virtuel de base local sur un serveur hôte de virtualisation des services Bureau à distance (RDV) spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BaseVmLocation* \[ dans\]
</dt> <dd>

Emplacement de la machine virtuelle de base.

</dd> <dt>

*FarmName* \[ dans\]
</dt> <dd>

Nom de la batterie de serveurs hôtes vers laquelle effectuer la copie.

</dd> <dt>

*GoldCacheLocation* \[ dans\]
</dt> <dd>

Emplacement du cache Gold.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RdvhManagement Win32**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





