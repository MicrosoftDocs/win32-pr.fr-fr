---
title: Méthode GetPatchProperties de la classe Win32_RDMSVirtualDesktopCollection
description: Récupère les propriétés d’un travail d’approvisionnement des mises à jour logicielles pour les machines virtuelles dans une collection de bureaux virtuels.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetPatchProperties
- Services Bureau à distance de la méthode GetPatchProperties, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode GetPatchProperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508846"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Méthode GetPatchProperties de la \_ classe Win32 RDMSVirtualDesktopCollection

Récupère les propriétés d’un travail d’approvisionnement des mises à jour logicielles pour les machines virtuelles dans une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartTime* \[ à\]
</dt> <dd>

Date et heure d’installation des mises à jour.

</dd> <dt>

*ForceLogOffTime* \[ à\]
</dt> <dd>

Date et heure auxquelles le système déconnecte les utilisateurs des ordinateurs virtuels.

</dd> <dt>

*JobGuid* \[ à\]
</dt> <dd>

**GUID** qui identifie de façon unique le travail d’approvisionnement.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

État du travail d’approvisionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





