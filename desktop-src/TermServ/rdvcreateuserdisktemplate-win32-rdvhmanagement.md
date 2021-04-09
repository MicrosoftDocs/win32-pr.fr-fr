---
title: Méthode RdvCreateUserDiskTemplate de la classe Win32_RdvhManagement
description: Crée un modèle de disque utilisateur, avec la taille maximale spécifiée, à l’emplacement spécifié.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvCreateUserDiskTemplate
- Services Bureau à distance de la méthode RdvCreateUserDiskTemplate, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvCreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743285"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a>Méthode RdvCreateUserDiskTemplate de la \_ classe Win32 RdvhManagement

Crée un modèle de disque utilisateur, avec la taille maximale spécifiée, à l’emplacement spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UserDisksStorageUrl* \[ dans\]
</dt> <dd>

Emplacement du stockage sur disque de l’utilisateur.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ dans\]
</dt> <dd>

Taille maximale du disque de l’utilisateur, en Go.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

Tous les disques utilisateur créés à l’aide de ce modèle auront la même taille maximale que le modèle.

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

 

 





