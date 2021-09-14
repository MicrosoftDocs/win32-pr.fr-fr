---
title: Méthode GetProvisioningProperties de la classe Win32_RDMSCollectionProperties
description: Récupère les propriétés de configuration de la collection de bureaux virtuels.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetProvisioningProperties
- Services Bureau à distance de la méthode GetProvisioningProperties, classe Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties de la classe Services Bureau à distance, méthode GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920123"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Méthode GetProvisioningProperties de la \_ classe Win32 RDMSCollectionProperties

Récupère les propriétés de configuration de la collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PoolVhdType* \[ à\]
</dt> <dd>

Spécifie le format de disque dur virtuel (VHD) du pool d’ordinateurs virtuels dans la collection.

<dt>

Clone
</dt> <dd>

Disque dur virtuel cloné.

</dd> <dt>

DiffDisk
</dt> <dd>

Disque dur virtuel de différenciation.

</dd> </dl> </dd> <dt>

*MasterVmLocation* \[ à\]
</dt> <dd>

Reçoit le chemin d’accès à l’image de machine virtuelle principale.

</dd> <dt>

*NamePrefix* \[ à\]
</dt> <dd>

Reçoit le préfixe de nom à ajouter au début des noms de machine virtuelle.

</dd> <dt>

*NameStartIndex* \[ à\]
</dt> <dd>

Index de début.

</dd> <dt>

*LocalVmLocation* \[ à\]
</dt> <dd>

Reçoit le chemin d’accès local aux ordinateurs virtuels sur les serveurs Hyper-V. Si ce paramètre a la valeur **null** ou s’il est vide, le répertoire par défaut de l’ordinateur virtuel est utilisé.

</dd> <dt>

*LocalGoldVmLocation* \[ à\]
</dt> <dd>

Reçoit le chemin d’accès local à l’image de disque dur virtuel Golden lorsque le paramètre *PoolVhdTpe* a la valeur « DiffDisk ». Si ce paramètre a la valeur **null** ou s’il est vide, le répertoire par défaut de l’ordinateur virtuel est utilisé.

</dd> <dt>

*RunFromSMB* \[ à\]
</dt> <dd>

Reçoit une valeur qui indique si la collection doit être exécutée à partir d’un partage SMB (Server Message Block). **True** pour exécuter les machines virtuelles à partir d’un partage SBM ; dispose **False**.

</dd> <dt>

*SMBLocation* \[ à\]
</dt> <dd>

Reçoit le chemin d’accès au partage SMB si le partage SMB est activé.

</dd> <dt>

*SMBStreaming* \[ à\]
</dt> <dd>

Reçoit une valeur qui indique si la diffusion SMB est activée. **True** si le partage SMB est activé ; dispose **False**.

</dd> <dt>

*VmDomain* \[ à\]
</dt> <dd>

Reçoit le nom de domaine des ordinateurs virtuels dans la collection.

</dd> <dt>

*VmOU* \[ à\]
</dt> <dd>

Reçoit l’unité d’organisation (OU) Active Directory des machines virtuelles de la collection.

</dd> <dt>

*ProductKey* \[ à\]
</dt> <dd>

Reçoit les clés de produit du système d’exploitation pour les machines virtuelles de la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSCollectionProperties Win32**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





