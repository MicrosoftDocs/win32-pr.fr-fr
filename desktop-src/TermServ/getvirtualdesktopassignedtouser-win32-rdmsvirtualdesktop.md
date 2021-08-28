---
title: Méthode GetVirtualDesktopAssignedToUser de la classe Win32_RDMSVirtualDesktop
description: Récupère le bureau virtuel affecté à l’utilisateur spécifié.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetVirtualDesktopAssignedToUser
- Services Bureau à distance de la méthode GetVirtualDesktopAssignedToUser, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce30afea4a95ed462bfb1b456788fa54f045097c16c3d65070cdb343e928237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059547"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>Méthode GetVirtualDesktopAssignedToUser de la \_ classe Win32 RDMSVirtualDesktop

Récupère le bureau virtuel affecté à l’utilisateur spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CollectionAlias* \[ dans\]
</dt> <dd>

Alias de la collection de bureaux virtuels qui contient le bureau virtuel.

</dd> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Nom d’utilisateur.

</dd> <dt>

*UserDomain* \[ dans\]
</dt> <dd>

Nom de domaine de l’utilisateur.

</dd> <dt>

*Vmname* \[ à\]
</dt> <dd>

Reçoit le nom de l’ordinateur virtuel du bureau virtuel.

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

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





