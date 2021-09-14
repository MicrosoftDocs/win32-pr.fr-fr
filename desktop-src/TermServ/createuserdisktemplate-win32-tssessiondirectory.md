---
title: Méthode CreateUserDiskTemplate de la classe Win32_TSSessionDirectory
description: Crée un modèle de disque utilisateur.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateUserDiskTemplate
- Services Bureau à distance de la méthode CreateUserDiskTemplate, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013372"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Méthode CreateUserDiskTemplate de la \_ classe Win32 TSSessionDirectory

Crée un modèle de disque utilisateur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UserDisksStorageUrl* \[ dans\]
</dt> <dd>

Emplacement du partage où sont stockés tous les disques utilisateur.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ dans\]
</dt> <dd>

Taille maximale en gigaoctets pour tous les disques utilisateur.

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

 

 





