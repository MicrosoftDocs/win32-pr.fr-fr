---
title: Méthode ProvisioningPrepJob de la classe Win32_RDMSVirtualDesktopCollection
description: Crée un travail d’approvisionnement de bureaux virtuels.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningPrepJob
- Services Bureau à distance de la méthode ProvisioningPrepJob, Win32_RDMSVirtualDesktopCollection interface
- Win32_RDMSVirtualDesktopCollection Services Bureau à distance de l’interface, méthode ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942043"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Méthode ProvisioningPrepJob de la \_ classe Win32 RDMSVirtualDesktopCollection

Crée un travail d’approvisionnement de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CollectionAlias* \[ dans\]
</dt> <dd>

Alias de la collection qui héberge le bureau virtuel.

</dd> <dt>

*VMHostName* \[ dans\]
</dt> <dd>

Nom d’hôte de l’ordinateur virtuel.

</dd> <dt>

*Vmname* \[ dans\]
</dt> <dd>

Nom de la machine virtuelle.

</dd> <dt>

*ExportToLocation* \[ dans\]
</dt> <dd>

Chemin d’accès complet de l’emplacement d’exportation du travail d’approvisionnement.

</dd> <dt>

*bSysPrep* \[ dans\]
</dt> <dd>

Indique si le travail d’approvisionnement représente un déploiement Sysprep.

</dd> <dt>

*Nomordinateur* \[ dans\]
</dt> <dd>

Nom de l’ordinateur qui héberge l’ordinateur virtuel.

</dd> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Nom d’utilisateur de l’administrateur de la machine virtuelle.

</dd> <dt>

*Mot de passe* \[ dans\]
</dt> <dd>

Mot de passe de l’administrateur de la machine virtuelle.

</dd> <dt>

*JobGuid* \[ à\]
</dt> <dd>

**GUID** qui identifie de façon unique le travail d’approvisionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





