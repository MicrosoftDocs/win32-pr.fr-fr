---
title: Méthode QueryOfflineInformation de la classe Win32_TSVm
description: Récupère les propriétés du serveur de bureau virtuel (VDS) actuel, mais uniquement lorsque le serveur est hors connexion.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode QueryOfflineInformation
- Services Bureau à distance de la méthode QueryOfflineInformation, classe Win32_TSVm
- Win32_TSVm de la classe Services Bureau à distance, méthode QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843845"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Méthode QueryOfflineInformation de la \_ classe Win32 TSVm

Récupère les propriétés du serveur de bureau virtuel (VDS) actuel, mais uniquement lorsque le serveur est hors connexion.

## <a name="syntax"></a>Syntaxe


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Créer* \[ à\]
</dt> <dd>

En cas de réussite, retourne la version de la build du VDS.

</dd> <dt>

*CurrentVersion* \[ à\]
</dt> <dd>

En cas de réussite, retourne la version actuelle du VDS.

</dd> <dt>

*INSTALLATIONTYPE* \[ à\]
</dt> <dd>

En cas de réussite, retourne le type d’installation du VDS.

</dd> <dt>

*EditionId* \[ à\]
</dt> <dd>

En cas de réussite, retourne l’ID d’édition du VDS.

</dd> <dt>

*SysPrepImageState* \[ à\]
</dt> <dd>

En cas de réussite, retourne l’état de l’image de préparation du système du VDS.

</dd> <dt>

*SysPrepMode* \[ à\]
</dt> <dd>

En cas de réussite, retourne le mode de préparation du système du VDS.

</dd> <dt>

*ProcArch* \[ à\]
</dt> <dd>

En cas de réussite, retourne une valeur indiquant l’architecture du processeur.

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

amd64

</dd> </dl> </dd> <dt>

*fIsVmbusCapable* \[ à\]
</dt> <dd>

en cas de réussite, indique si le système est apte à la compatibilité VMBus.

</dd> <dt>

*fIsRdvIcInstalled* \[ à\]
</dt> <dd>

En cas de réussite, indique si RDVIC est installé.

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

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





