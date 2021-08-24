---
title: Méthode EnableUserVhd de la classe Win32_TSSessionDirectory
description: Active un disque dur virtuel de profil utilisateur sur un serveur hôte hôte.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableUserVhd
- Services Bureau à distance de la méthode EnableUserVhd, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19e042b51c7060e4d4c2a8302a87b2d27ee2cf89608a9831cb3497fd0566689a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871739"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Méthode EnableUserVhd de la \_ classe Win32 TSSessionDirectory

Active un disque dur virtuel de profil utilisateur sur un serveur hôte hôte.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UvhdShareUrl* \[ dans\]
</dt> <dd>

Emplacement du partage où sont stockés tous les disques durs virtuels de profil utilisateur.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ dans\]
</dt> <dd>

Stratégie d’itinérance pour le disque dur virtuel du profil utilisateur.

</dd> </dl>

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

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





