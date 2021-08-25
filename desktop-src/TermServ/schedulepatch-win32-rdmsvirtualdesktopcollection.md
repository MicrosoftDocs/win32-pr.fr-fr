---
title: Méthode SchedulePatch de la classe Win32_RDMSVirtualDesktopCollection
description: Planifie un travail d’approvisionnement des mises à jour logicielles qui installe les mises à jour logicielles sur les machines virtuelles d’une collection de bureaux virtuels.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SchedulePatch
- Services Bureau à distance de la méthode SchedulePatch, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb29eb42f0f1d13ff1bf234c6fb41b8f414317a4b723af9a6d215cf25fa2ec95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865509"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Méthode SchedulePatch de la \_ classe Win32 RDMSVirtualDesktopCollection

Planifie un travail d’approvisionnement des mises à jour logicielles qui installe les mises à jour logicielles sur les machines virtuelles d’une collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartTime* \[ dans\]
</dt> <dd>

> [!Note]  
> Le système ne déconnecte pas les utilisateurs des ordinateurs virtuels avant l’heure spécifiée dans le paramètre *ForceLogOffTime* .

 

Date et heure d’installation des mises à jour.

</dd> <dt>

*ForceLogOffTime* \[ dans\]
</dt> <dd>

Date et heure auxquelles le système déconnecte les utilisateurs des ordinateurs virtuels.

</dd> <dt>

*JobInputXml* \[ dans\]
</dt> <dd>

Chaîne au format XML qui contient les informations de la tâche de mise à jour logicielle.

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

 

 





